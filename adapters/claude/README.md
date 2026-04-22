# Claude Adapter

This adapter explains how AEHF is delivered into Claude-style environments.

The AEHF method remains the same.
What changes is how startup context, repository memory, and execution rules are exposed to the tool.

---

## Adapter purpose

The Claude adapter exists to:
- create a short, strict startup contract
- reduce ambiguity at session start
- force reading order before non-trivial work
- keep durable detail in repository memory instead of bloating the adapter entry point

---

## Primary entry point

File:
- `CLAUDE.md`

This file is the high-priority bootstrap contract for Claude-style environments.
It should remain short enough to be usable, but strong enough to enforce the method.

Its role is to direct the tool into the real sources of truth rather than trying to hold the entire project in one file.

---

## Required entry sequence

For non-trivial work, begin with:

1. `README.md`
2. `docs/constitution/CONSTITUTION.md`
3. `docs/architecture/INVENTORY.md`
4. `docs/standards/TASK_DEPTH_POLICY.md`
5. `docs/standards/CODING_STANDARDS.md`
6. `docs/standards/DOC_UPDATE_POLICY.md`
7. `AGENTS.md`

Then consult task-specific context as needed:
- relevant files under `docs/domains/`
- relevant package under `specs/`
- related decisions under `docs/decisions/`
- gaps or discrepancies under `docs/gaps/`

---

## Operating expectations

When using Claude with AEHF, the expected behavior is:

- classify task depth before deciding process or artifacts
- preserve behavior unless intentional change is documented
- prefer incremental change over rewrite
- use repository memory instead of re-explaining context in every interaction
- update docs, specs, and changelog when meaningful change occurs
- distinguish facts from assumptions
- escalate to human validation when risk or ambiguity is high

---

## Why this adapter is structured this way

Claude-style environments benefit from a strong startup contract, but they also benefit when durable detail remains outside the bootstrap file.

This adapter therefore separates:
- a concise entry point (`CLAUDE.md`)
- durable operational memory (`docs/`)
- structured change packages (`specs/`)
- reusable workflows (`prompts/`)

That separation keeps the method strong without turning the adapter into a monolithic context dump.

---

## Suggested usage pattern

A practical usage flow is:

1. start from `CLAUDE.md`
2. follow the mandatory reading order
3. classify task depth
4. inspect the relevant domain, spec, decision, and gap files
5. execute incrementally
6. update project memory as part of the same change package

---

## What this adapter is not

This adapter is not:
- a full substitute for repository documentation
- a giant project memory file
- a separate method from AEHF
- a justification for skipping specs or standards

It is the Claude-specific bootstrap mechanism for the same universal AEHF operating model.

---

## Final rule

If any Claude-specific shortcut conflicts with the AEHF constitution or standards, the core method wins.
