# Surgical Dev Extension

A Gemini CLI extension to enforce **software engineering standards**: Surgical precision, senior pragmatism, and goal-driven execution.

## Why Use This?

Sometimes AI coding agents are **"too helpful."** This often manifests as:
1. **Drive-by Refactoring:** Changing quote styles, docstrings, or formatting in lines unrelated to the task.
2. **Speculative Over-engineering:** Adding "just-in-case" configuration or complex abstractions for simple logic.
3. **Hidden Guessing:** Implementing an interpretation of a vague request without asking for clarification.
4. **Fixing without Reproducing:** Changing code to fix a bug before proving the bug exists with a failing test.

This extension handle these behaviors.

## Operational Features

- **Dense Context (`GEMINI.md`)**: High-density instructions for minimal token overhead in every turn.
- **Audit Command (`/surgical:audit`)**: Reviews your proposed strategy or latest diff for over-engineering or non-surgical changes.
- **Reviewer Sub-agent (`surgical-reviewer`)**: Delegate code reviews to a specialist who enforces surgical precision without cluttering the main history.
- **Agent Skill (`surgical-standards`)**: Manually activate for a deep "behavioral reset" during complex tasks. (≈500 tokens)

## How to Use the Surgical Dev Workflow

### 1. The Strategy Audit (`/surgical:audit`)
**When:** After the model proposes a plan, but before you say "Go."
**How:** Type `/surgical:audit`.
**Why:** It forces the model to review its own proposal for **Scope Creep** (refactoring a whole file for a 1-line fix) and **Speculative Bloat** (adding abstractions you didn't ask for).

### 2. The Surgical Reviewer (`gemini delegate surgical-reviewer`)
**When:** You've finished a task and want to ensure no "noise" (style changes, unrelated edits) leaked into the diff.
**How:** Run:
```bash
gemini delegate surgical-reviewer "Review my last changes in src/utils.ts"
```
**Why:** This sub-agent has zero tolerance for non-surgical edits. It will flag quote changes, unnecessary classes, and missing verification steps.

### 3. The Behavioral Reset (`Activate surgical-standards`)
**When:** The model is "looping," getting confused, or producing overly complex code.
**How:** Type `Activate surgical-standards skill`.
**Why:** This loads the full, detailed standards into the active context. Use this as an "emergency brake" to return the model to a pragmatic, surgical mindset.

### 4. Continuous Enforcement (`GEMINI.md`)
**When:** Every single turn.
**How:** Automatic.
**Why:** The `GEMINI.md` provides a background constraint, reminding the model to reproduce bugs before fixing them, minimize code length, and remove orphans (imports/vars).

## Installation

To install the extension directly from GitHub:
```bash
gemini extensions install https://github.com/sniperwolf/surgical-dev-extension
```

### Local Development (Optional)
If you are developing or customizing the extension locally:
1.  **Link the extension:**
    ```bash
    gemini extensions link YOUR_PATH_TO/surgical-dev-extension
    ```
2.  **Restart your session.**
