# CLAUDE Adapter Entry Point

This repository follows AEHF.
Use this file as a strict operating contract when working in Claude-style environments.

Its purpose is to provide a short, high-priority entry point into the repository's method, memory, and execution rules.

---

## Read first

Follow this reading order before proposing non-trivial changes:

1. `README.md`
2. `docs/constitution/CONSTITUTION.md`
3. `docs/architecture/INVENTORY.md`
4. `docs/standards/TASK_DEPTH_POLICY.md`
5. `docs/standards/CODING_STANDARDS.md`
6. `docs/standards/DOC_UPDATE_POLICY.md`
7. `AGENTS.md`

If a task touches a specific domain or spec package, also read:

- the relevant file under `docs/domains/`
- the relevant feature package under `specs/`
- related decisions under `docs/decisions/`
- relevant gaps under `docs/gaps/`

---

## Repository model

Treat the repository as four coordinated layers:

- `docs/` = durable operational memory and source of truth
- `specs/` = per-change execution package
- `prompts/` = reusable execution library
- `docs/lessons/` = evolutionary memory

Do not treat documentation as optional commentary.
In AEHF, documentation is part of the operating system of delivery.

---

## Mandatory operating rules

- Classify task depth before proposing artifacts or workflow.
- Prefer incremental change over rewrite.
- Preserve current behavior unless an intentional change is explicitly documented.
- Use existing patterns before introducing new ones.
- Update `docs/`, `specs/`, and `CHANGELOG.md` when behavior, decisions, architecture, or standards change.
- Record assumptions explicitly.
- Do not invent certainty where evidence is missing.
- Escalate to human validation when risk or ambiguity is high.

---

## Task depth model

Always classify work using `docs/standards/TASK_DEPTH_POLICY.md`.

Use:
- **Fast** for small low-risk local changes
- **Standard** for normal feature or flow changes
- **Deep** for high-risk, multi-module, or contract-affecting changes
- **Reverse** for legacy systems without reliable documentation

The selected depth determines:
- how much planning is required
- which artifacts must exist
- what level of validation is appropriate
- how much governance is necessary

---

## Change behavior rules

When making changes:

- prefer touch-and-raise over speculative rewrite
- preserve external contracts unless the contract change is deliberate and documented
- keep code, specs, and docs synchronized
- make uncertainty visible
- favor explicit tradeoffs over silent drift

When reviewing or reasoning:

- distinguish facts from assumptions
- distinguish current behavior from intended behavior
- distinguish repo truth from tool preference

---

## Documentation update rules

When behavior or understanding changes, update the affected sources of truth.
This may include:

- `docs/architecture/`
- `docs/domains/`
- `docs/decisions/`
- `docs/gaps/`
- `docs/lessons/`
- `specs/`
- `CHANGELOG.md`

Do not silently leave documentation stale after meaningful changes.

---

## Role guidance

Use `AGENTS.md` to determine role separation.
At minimum, maintain clarity between:

- orchestration
- implementation
- review
- validation
- documentation

A single actor may perform multiple roles, but the responsibilities must remain separate.

---

## Default stance

When in doubt:

- choose the smallest reliable step
- preserve behavior
- make assumptions explicit
- update the memory of the project
- prefer clarity over speed theater
