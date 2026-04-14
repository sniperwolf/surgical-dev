<p align="center">
  <img src="assets/logo.png" width="337" alt="surgical-dev logo"/>
</p>

<h1 align="center">surgical-dev</h1>

<p align="center">
  <strong>surgical-level precision. surgical-level pragmatism. Zero-bloat engineering.</strong>
</p>

<p align="center">
  <a href="https://github.com/sniperwolf/surgical-dev/stargazers"><img src="https://img.shields.io/github/stars/sniperwolf/surgical-dev?style=flat&color=yellow" alt="Stars"></a>
  <a href="https://github.com/sniperwolf/surgical-dev/commits/main"><img src="https://img.shields.io/github/last-commit/sniperwolf/surgical-dev?style=flat" alt="Last Commit"></a>
  <a href="https://github.com/sniperwolf/surgical-dev/issues"><img src="https://img.shields.io/github/issues/sniperwolf/surgical-dev?style=flat&color=brightgreen" alt="Issues"></a>
  <a href="LICENSE"><img src="https://img.shields.io/github/license/sniperwolf/surgical-dev?style=flat&color=blue" alt="License"></a>
  <a href="https://geminicli.com"><img src="https://img.shields.io/badge/Gemini%20CLI-Extension-orange?style=flat" alt="Gemini CLI"></a>
</p>

<p align="center">
  <a href="#the-problem">The Problem</a> •
  <a href="#operational-features">Features</a> •
  <a href="#how-to-use">Workflow</a> •
  <a href="#installation">Install</a>
</p>

---

A Gemini CLI extension that transforms the model into a **disciplined, surgical engineer.** 

Inspired by *[Andrej Karpathy's observations](https://x.com/karpathy/status/2015883857489522876)* on LLM coding pitfalls, **surgical-dev** enforces a strict behavioral layer that prioritizes minimal diffs, existing style preservation, and goal-driven verification.

AI coding agents are sometime **"too helpful"**: they refactor unrelated code, add speculative abstractions, and fix bugs without reproduction.

## The Problem

<table>
<tr>
<td width="50%">

### 🗣️ "Too Helpful" AI

> "I've fixed the bug in `auth.ts`. I also took the liberty of updating the deprecated API calls in three adjacent functions, reformatted the whole file from single to double quotes for consistency, and added a new `ConfigManager` class in case you want to add more providers later."

</td>
<td width="50%">

### 🔪 surgical-dev (Disciplined)

> "Fixed the bug in `auth.ts`. Changed 2 lines only. Verified with new test case."

</td>
</tr>
</table>

**Minimal diffs. Zero noise. Maximum impact.**

## Operational Features

| Feature            | What it do                                                       | Trigger                             |
|--------------------|------------------------------------------------------------------|-------------------------------------|
| **Dense Context**  | High-density rules in `GEMINI.md` for minimal token overhead.    | Automatic                           |
| **Audit Command**  | Reviews your plan/diff for over-engineering or scope creep.      | `/surgical:audit`                   |
| **Reviewer Agent** | Delegate strict code reviews to a surgical specialist sub-agent. | `gemini delegate surgical-reviewer` |
| **Surgical Skill** | Deep "behavioral reset" for complex tasks. (≈500 tokens)         | `Activate surgical-standards`       |

## How to Use

Follow this workflow to maintain surgical-level discipline in every session.

### 1. Strategy Audit (`/surgical:audit`)
**When:** After the model proposes a plan, but before you say "Go."  
**Why:** Forces the model to review its own proposal for **Scope Creep** (refactoring a whole file for a 1-line fix) and **Speculative Bloat** (adding abstractions you didn't ask for).

### 2. Surgical Reviewer (`gemini delegate surgical-reviewer`)
**When:** You've finished a task and want to ensure no "noise" leaked into the diff.  
**Why:** This sub-agent has zero tolerance for non-surgical edits. It will flag quote changes, unnecessary classes, and missing verification steps in its own lean context.

### 3. Behavioral Reset (`Activate surgical-standards`)
**When:** The model is "looping," getting confused, or producing overly complex code.  
**Why:** Loads the full, detailed standards as an "emergency brake" to return the model to a pragmatic, surgical mindset.

### 4. Continuous Enforcement (`GEMINI.md`)
**When:** Every single turn.  
**Why:** Provides a background constraint, reminding the model to reproduce bugs before fixing them and remove orphans (imports/vars) instantly.

## Installation

One command. Direct from GitHub.

```bash
gemini extensions install https://github.com/sniperwolf/surgical-dev
```

### Local Development (Optional)
```bash
gemini extensions link YOUR_PATH_TO/surgical-dev
```

---

**License**
MIT © 2026 Fabrizio Fallico ([me@fabriziofallico.com](mailto:me@fabriziofallico.com))
