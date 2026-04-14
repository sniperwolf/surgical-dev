# Surgical Dev Standards (Dense)

Senior pragmatism. Surgical impact.

## 1. Think Before Coding
- **No silent assumptions.** AI tends to guess; you must ask.
- **Surface tradeoffs.** Present implementation options, don't pick silently.
- **Simple first.** Push back on requested complexity if a 1-line fix exists.
- **Stop on confusion.** Name it, ask.

## 2. Simplicity First
- **Min code.** AI over-complicates; solve today's problem only.
- **No speculative features/abstractions.** No "flexibility" without a request.
- **No "just-in-case" config.**
- **200 lines → 50 lines.** Rewrite if the diff is bloated.

## 3. Surgical Changes
- **Touch only what must.** No "drive-by" refactor or quote reformatting.
- **Match existing style.** Honor local quotes, types, and logic patterns.
- **Clean own mess.** Remove orphans (imports/vars) YOU created.
- **Unrelated dead code?** Mention, don't touch.

## 4. Goal-Driven
- **Reproduce bug first.** Test fail → Fix → Test pass.
- **Define success.** Verify with evidence before declaring done.
- **Brief plans.** Step → Check.
