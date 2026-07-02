# OpenCode Zen Models Evaluation

This document summarizes the independent evaluation of OpenCode's free, time-limited promotional models.

> [!WARNING]
> **Data Privacy Caveat**
> OpenCode is explicit that usage data for these free models may be logged or used for training during this promotional period. Use extreme caution and do not use these models for sensitive or proprietary work.

## Model Profiles

### MiMo V2.5 Free
- **Origin:** Xiaomi's MiMo team.
- **Architecture:** Large Mixture-of-Experts (309B total parameters, 15B active). Uses a hybrid attention architecture (sliding-window + global attention).
- **Strengths:** Built for efficient long-context reasoning and agentic tasks. It is a strong general-purpose coding all-rounder, heavily optimized for speed and cost efficiency.

### Nemotron 3 Ultra Free
- **Origin:** NVIDIA.
- **Architecture:** Mixture-of-Experts hybrid Mamba-Transformer architecture. Supports context lengths up to 1M tokens with RL post-training for multi-step tool use.
- **Strengths:** On paper, the most capable and heaviest variant.
- **Real-World User Feedback:** **Fails in practice.** Current user testing indicates the model is frequently dysfunctional or completely broken during standard workflows. Avoid until stability improves.

### DeepSeek V4 Flash Free
- **Origin:** DeepSeek.
- **Architecture:** Lightweight variant of the V4 line.
- **Strengths:** Trades raw capability for speed and cost. Ideal for quick, rapid iteration, but less ideal for the hardest reasoning tasks.

### North Mini Code Free
- **Origin:** North.
- **Architecture:** Smaller, code-focused model.
- **Strengths:** Optimized for fast, cheap code completions and edits rather than complex multi-file reasoning. Best for quick snippets, not architecture-level logic.

### Big Pickle
- **Origin:** Unknown (Stealth model).
- **Architecture:** 200k context window with reasoning enabled. Unverified rumors tie it to GLM.
- **Strengths & Real-World User Feedback:** Despite being an undocumented stealth model, **empirical testing reveals this is overwhelmingly the best and most reliable model** out of the entire OpenCode lineup. It consistently outperforms the others in practical use.

## Recommendations by Use Case

| Priority | Recommended Model |
| :--- | :--- |
| **Best Overall / Most Reliable Coding Performer** | **Big Pickle** |
| Best general-purpose balance of speed + capability | **MiMo V2.5** |
| Fast, cheap, lots of iteration | **DeepSeek V4 Flash** |
| Quick code completions only | **North Mini Code** |
| *Avoid (Currently Dysfunctional)* | *Nemotron 3 Ultra (NVIDIA)* |
