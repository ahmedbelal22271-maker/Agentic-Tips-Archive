# Claude Official Guidance & Docs Map

This document consolidates Anthropic's official Claude Prompting Best Practices and provides a directory map for Claude Code capabilities, serving as a master reference for agentic development.

## 1. Claude Prompting Best Practices

When programming Claude, strictly adhere to these official guidelines to ensure maximum reliability and performance:

### Be Clear and Direct
- **Clarity over politeness:** Claude responds best to clear, direct instructions. You do not need to say "please" or "thank you."
- **Assign a Role (System Prompting):** Always give Claude a specific role or persona (e.g., "You are an expert Python developer" or "You are a senior UX designer"). This grounds the model's responses in the correct domain.
- **Use XML Tags:** Claude is specifically trained to recognize and heavily weight information enclosed in XML tags (e.g., `<instructions>`, `<data>`, `<output_format>`). Use these to cleanly separate your prompt's rules, data, and expected output structure.

### Provide Examples (Few-Shot Prompting)
- Do not just describe what you want; **show** what you want.
- Provide 2-3 examples of perfect input-output pairs inside your prompt (using `<example>` tags) to drastically reduce formatting errors and hallucinations.

### Let Claude Think
- **The `<thinking>` tag:** Before Claude produces its final output, instruct it to map out its logic inside `<thinking>` tags.
- Forcing Claude to write out its reasoning step-by-step prevents logic skips and compounding errors in complex tasks.
- *Example:* "First, analyze the problem inside `<thinking>` tags. Then, provide the final solution."

### Break Down Complex Tasks
- If a task requires multiple distinct steps, do not give Claude one massive prompt.
- Break the task into a sequential chain of smaller prompts (prompt chaining), or explicitly number the steps Claude must take in its response.

## 2. Claude Code Documentation Map

For configuring local terminal or IDE-based agentic workflows, Anthropic provides Claude Code. Below is the structural map of its core capabilities and where to find them in the official docs (`https://code.claude.com/docs/en/`):

### Core Concepts
- **How Claude Code Works:** The agentic loop, models, tools, and environments.
- **Features Overview:** Context costs and feature layering.
- **Context Window & Prompt Caching:** How to manage context limits, cache lifetimes, and actions that invalidate the prompt cache (e.g., switching models vs editing files).

### Configuration & Memory
- **Memory (`CLAUDE.md`):** How to structure project-level instructions, use `AGENTS.md`, and organize `.claude/rules/`.
- **Permission Modes:**
  - `acceptEdits`: Auto-approve file edits.
  - `plan`: Analyze before editing.
  - `auto`: Eliminate permission prompts (autonomous mode).
  - `bypassPermissions`: Skip all safety checks.
- **Common Workflows:** Prompt recipes for bug fixing, refactoring, code reviews, and using subagents for research.

### Integrations & Tooling
- **Web & Desktop Clients:** Managing remote cloud sessions, teleporting tasks, and using Claude Code natively on Windows/Linux.
- **VS Code & JetBrains:** IDE extensions, prompt boxes, and built-in MCP (Model Context Protocol) servers.
- **CI/CD:** Using Claude Code in GitHub Actions, GitHub Enterprise, and GitLab CI/CD for autonomous code reviews.
- **Security Guidance:** Plugins for security checks and adversarial review steps.
