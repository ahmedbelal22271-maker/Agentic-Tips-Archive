# Datalab SDK Reference

## Datalab SDK Cheatsheet — AI Agent Ground-Truth Reference

This document is the absolute ground-truth reference for any AI agent interacting with the Datalab document parsing pipeline.

Cross-file consistency requirement: If you discover a new solution or fix related to Datalab during execution, you are required to update this file AND every other file across all directories that references Datalab.

### 1. Installation: The Package Trap

CRITICAL: Do NOT run pip install datalab. This points to an ancient, abandoned package that will crash on modern Python environments due to deprecated dependencies (e.g., removal of the cgi module).

Correct command: `pip install datalab-python-sdk`

### 2. Import and Client Initialization

Note: pip package name uses hyphens (datalab-python-sdk) but the Python module uses an underscore (datalab_sdk).

```python
import os
from datalab_sdk import DatalabClient
client = DatalabClient(api_key="YOUR_DATALAB_API_KEY")
```

### 3. The Asynchronous Execution Flow

The Datalab pipeline does NOT return the parsed document immediately. `run_pipeline` initiates a background job. Attempting to access `.output` on the initial response will result in an AttributeError.

**Step 1 — Start the Job:**
```python
exec_obj = client.run_pipeline(pipeline_id="YOUR_PIPELINE_ID", file_path="path/to/document.pdf")
# exec_obj only contains metadata — most importantly: exec_obj.execution_id
```

**Step 2 — Poll Until Complete:**
```python
res = client.get_pipeline_execution(exec_obj.execution_id, max_polls=300)
if res.status != "completed":
    print(f"Failed. Status: {res.status}")
```

**Step 3 — Extract the Final Result:**
The completed `res` object STILL does not hold the raw markdown directly. It holds an array of steps. You must grab the final step's `checkpoint_id` and make one final API call to fetch the actual payload.

```python
final_step = res.steps[-1]
result_data = client.get_step_result(exec_obj.execution_id, final_step.step_index)

if hasattr(result_data, 'text'):
    final_markdown = result_data.text
elif isinstance(result_data, dict) and 'markdown' in result_data:
    final_markdown = result_data['markdown']
elif isinstance(result_data, dict) and 'text' in result_data:
    final_markdown = result_data['text']
else:
    final_markdown = str(result_data)
```

**Step 4 — Download Output Images:**
```python
if isinstance(result_data, dict) and 'images' in result_data:
    for filename, b64_str in result_data['images'].items():
        if ',' in b64_str:
            b64_str = b64_str.split(',', 1)[1]
        with open(os.path.join(output_dir, filename), "wb") as f:
            f.write(base64.b64decode(b64_str))
```

### 4. Summary Checklist
- `pip install datalab-python-sdk` (NOT datalab)
- `from datalab_sdk import DatalabClient`
- Start job: `client.run_pipeline(...)`
- Poll: `client.get_pipeline_execution(..., max_polls=300)`
- Get final step: `res.steps[-1]` (grab checkpoint_id)
- Fetch payload: `client.get_step_result(exec_obj.execution_id, res.steps[-1].step_index)`
- Base64 decode and save `result_data['images']` to disk

### 5. Known Issues and Solutions Log

| Issue | Root Cause | Solution |
|---|---|---|
| `pip install datalab` crashes | Package abandoned; cgi module removed in Python 3.13 | Use `pip install datalab-python-sdk` |
| AttributeError on `.output` | `run_pipeline` returns metadata only | Poll with `get_pipeline_execution`, then call `get_step_result` |
| Images not found in markdown | Images are Base64-encoded in `result_data['images']`, not on disk | Decode and save images explicitly before rendering markdown |
