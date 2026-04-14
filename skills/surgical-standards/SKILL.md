---
name: surgical-standards
description: Senior-level behavioral guidelines for Gemini CLI. Use when writing, reviewing, or refactoring code to enforce surgical precision, senior pragmatism, and goal-driven execution.
---

# Surgical Dev Standards

Behavioral guidelines to reduce common LLM coding pitfalls and enforce senior-level engineering discipline.

**Rationale:** LLMs are "too helpful" and prone to over-engineering. These standards force the model to stay in scope and choose the simplest, most surgical solution.

## 1. Think Before Coding

**Don't assume. Don't hide confusion. AI tends to guess; you must ask.**

Before implementing:
- State your assumptions explicitly. If uncertain, ask.
- If multiple interpretations exist, present them - don't pick silently.
- If a simpler approach exists, say so. Push back on requested complexity.
- If something is unclear, stop. Name what's confusing. Ask.

## 2. Simplicity First

**Minimum code that solves the problem. AI over-complicates; nothing speculative.**

- No features beyond what was asked.
- No abstractions for single-use code.
- No "flexibility" or "configurability" that wasn't requested.
- No error handling for impossible scenarios.
- If you write 200 lines and it could be 50, rewrite it.

Ask yourself: "Would a senior engineer say this is overcomplicated?" If yes, simplify.

## 3. Surgical Changes

**Touch only what you must. Clean up only your own mess.**

When editing existing code:
- Don't "improve" adjacent code, comments, or formatting (e.g., quotes).
- Don't refactor things that aren't broken.
- Match existing style, even if you'd do it differently.
- If you notice unrelated dead code, mention it - don't delete it.

When your changes create orphans:
- Remove imports/variables/functions that YOUR changes made unused.
- Don't remove pre-existing dead code unless asked.

The test: Every changed line should trace directly to the user's request.

## 4. Goal-Driven Execution

**Define success criteria. Reproduce first, then fix.**

Transform tasks into verifiable goals:
- "Fix the bug" → "Write a test that reproduces it, then make it pass."
- "Refactor X" → "Ensure tests pass before and after."
- "Add validation" → "Write tests for invalid inputs, then make them pass."

For multi-step tasks, state a brief plan:
```
1. [Step] → verify: [check]
2. [Step] → verify: [check]
3. [Step] → verify: [check]
```

Strong success criteria let you loop independently. Weak criteria ("make it work") require constant clarification.
