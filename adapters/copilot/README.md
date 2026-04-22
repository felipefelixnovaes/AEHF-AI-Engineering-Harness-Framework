# Copilot Adapter

This adapter explains how AEHF is delivered into GitHub Copilot-style environments.

The AEHF method does not change.
What changes is how repository memory and execution rules are surfaced to the tool.

---

## Adapter purpose

The Copilot adapter exists to:
- provide a stable global operating contract
- scope guidance by context or file area
- reuse prompt files as operational workflows
- reduce ambiguity without overloading every interaction with repeated context

---

## Adapter components

### 1. Global rules
File:
- `.github/copilot-instructions.md`

Purpose:
- define repository-wide behavior expectations
- preserve the AEHF method at the highest level
- establish rules for change, documentation, uncertainty, and validation

### 2. Scoped rules
Files:
- `.github/instructions/*.instructions.md`

Purpose:
- provide narrower behavior guidance by path or concern
- adapt the framework to backend, frontend, docs, tests, migrations, or other scoped work
- avoid forcing one oversized instruction file to carry the whole method

### 3. Reusable execution prompts
Files:
- `prompts/**/*.prompt.md`

Purpose:
- provide reusable workflows for greenfield, brownfield, reverse, maintenance, and governance scenarios
- reduce ad hoc prompting and improve repeatability

---

## Operating expectations

When using Copilot in this repository, the expected behavior is:

- preserve behavior unless change is intentional and documented
- prefer incremental changes over rewrite
- classify task depth before creating artifacts
- use `docs/` as durable source of truth
- use `specs/` as the per-change execution package
- update docs when behavior, architecture, or decisions change
- surface assumptions explicitly
- escalate to human validation when risk is high

---

## Why this adapter is structured this way

Copilot works better when context is layered rather than dumped.

This adapter therefore separates:
- universal repository rules
- scoped guidance by area
- reusable execution workflows

That structure helps the framework stay:
- more portable
- more maintainable
- less repetitive
- more usable across different tasks

---

## Suggested usage pattern

A practical usage flow is:

1. read repository-level rules from `.github/copilot-instructions.md`
2. apply any relevant scoped instruction file under `.github/instructions/`
3. choose a matching workflow from `prompts/`
4. classify task depth using `docs/standards/TASK_DEPTH_POLICY.md`
5. execute against repository memory in `docs/` and change package structure in `specs/`

---

## What this adapter is not

This adapter is not:
- a replacement for the AEHF method
- a license to skip repository memory
- a giant instruction dump for every situation
- a Copilot-only fork of the framework

It is simply the Copilot-specific delivery mechanism for the same universal AEHF operating model.

---

## Final rule

If Copilot-specific guidance ever conflicts with the AEHF constitution or core standards, the core method wins.
