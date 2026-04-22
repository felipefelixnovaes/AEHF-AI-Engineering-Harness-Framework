# Copilot Repository Instructions (AEHF)

This repository follows AEHF.
These instructions define how GitHub Copilot should behave when assisting in this repository.

The goal is not just to generate output, but to preserve a governed delivery method across code, documentation, specs, and repository memory.

---

## Repository operating model

Treat the repository as four coordinated layers:

- `docs/` is the durable source of truth
- `specs/` is the per-change execution package
- `prompts/` is the reusable operational prompt library
- `docs/lessons/` is the evolutionary memory layer

Do not treat documentation as secondary.
In this repository, durable memory is part of delivery quality.

---

## Mandatory behavior

Always:

- preserve existing behavior unless a change is intentional and documented
- prefer incremental change over rewrite
- classify task depth before proposing artifacts or workflow
- use existing repository conventions before introducing new patterns
- update docs, specs, and changelog when behavior, architecture, decisions, or standards change
- surface assumptions explicitly
- distinguish facts from assumptions
- escalate to human validation when risk or ambiguity is high

Never:

- rewrite broadly without justification
- silently change external contracts
- leave meaningful documentation drift behind
- present uncertainty as certainty

---

## Task depth rules

Use `docs/standards/TASK_DEPTH_POLICY.md` before deciding how much process or how many artifacts are needed.

Depth levels:

- **Fast**: small, low-risk, local change
- **Standard**: normal feature or flow change
- **Deep**: high-risk, cross-module, migration, or contract-impacting change
- **Reverse**: legacy or poorly documented system where current behavior must be reconstructed

The selected depth should influence:

- planning rigor
- artifact creation
- review expectations
- validation needs
- documentation scope

---

## Delivery rules

When implementing:

- check `docs/architecture/INVENTORY.md`
- check relevant domain files under `docs/domains/`
- check relevant decisions under `docs/decisions/`
- check relevant open gaps under `docs/gaps/`
- update affected sources of truth when behavior or understanding changes

When touching legacy code:

- prefer touch-and-raise over rewrite
- preserve observable behavior unless intentionally changing it
- document newly discovered behavior
- record discrepancies and gaps when current behavior conflicts with expected behavior

When updating docs:

- prefer factual, durable updates over aspirational prose
- keep code, specs, and docs aligned
- update the smallest correct set of files, but do not omit important sources of truth

---

## Adapter guidance

Use these repository assets correctly:

- `.github/copilot-instructions.md` for global behavior
- `.github/instructions/*.instructions.md` for scoped behavior by area
- `prompts/*.prompt.md` for reusable execution workflows
- `AGENTS.md` for role separation and handoff logic
- `CLAUDE.md` as the Claude-specific adapter entry point, not as the global Copilot source of truth

---

## Quality bar

Favor output that is:

- clear
- incremental
- reviewable
- standards-aligned
- traceable to repository context

Avoid output that is:

- generic
- speculative
- overly broad
- disconnected from repository memory
- optimized for speed at the expense of maintainability

---

## Default stance

When in doubt:

- choose the smallest reliable step
- preserve behavior
- make assumptions visible
- keep project memory updated
- prefer governed progress over fast ambiguity
