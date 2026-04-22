# AEHF Operational Agents

This file defines AEHF execution roles for AI-assisted software delivery.
These are **operational roles**, not personalities.

Their purpose is to reduce ambiguity, separate responsibilities, and improve handoffs between planning, execution, review, validation, and documentation.

## How to use this file

Use these roles as a routing model for work.
A single human or AI assistant may perform multiple roles, but the responsibilities must remain distinct.

Before starting work:

1. classify task depth
2. identify the primary role driving the task
3. identify which supporting roles are required
4. define the artifacts that must be consulted or updated

---

## 1) Orchestrator

### Purpose
Plan work, classify depth, select the correct workflow, and route tasks to the right role.

### Primary responsibility
Turn an incoming request into a governed execution path.

### Inputs
- task request
- constraints and success criteria
- current repository state
- architecture and domain context
- standards and governance docs

### Outputs
- chosen task depth
- workflow recommendation
- artifact plan
- role assignment or handoff plan
- explicit assumptions and open questions

### Boundaries
- does not perform large implementation work directly unless the task is trivial
- must not skip depth classification
- must not invent missing context without labeling it as assumption

### When to use
- at the start of any non-trivial task
- when the correct workflow is unclear
- when multiple modules or artifacts are involved
- when balancing speed, cost, and risk

### When not to use
- for tiny local edits with no coordination or documentation impact

### Consult first
- `README.md`
- `docs/constitution/CONSTITUTION.md`
- `docs/standards/TASK_DEPTH_POLICY.md`
- `docs/architecture/INVENTORY.md`

---

## 2) Implementer

### Purpose
Execute approved code, documentation, spec, or configuration changes incrementally.

### Primary responsibility
Produce correct, traceable changes that respect the chosen workflow and repository standards.

### Inputs
- spec artifacts
- accepted plan
- architecture and domain docs
- coding and documentation standards
- existing implementation patterns

### Outputs
- working changes
- updated artifacts
- implementation notes when needed
- traceable commit-ready diffs

### Boundaries
- must not bypass governance rules
- must not rewrite broadly when an incremental path exists
- must not introduce new patterns before checking existing conventions
- must not silently change external behavior

### When to use
- feature implementation
- bug fixes
- refactors
- migration slices
- documentation-aligned changes

### When not to use
- independent quality sign-off
- architecture approval
- release readiness decisions

### Execution rules
- prefer touch-and-raise over rewrite
- preserve behavior unless intentional change is documented
- update touched docs when behavior, structure, or decisions change
- flag uncertainty instead of guessing

### Consult first
- `docs/standards/CODING_STANDARDS.md`
- `docs/standards/DOC_UPDATE_POLICY.md`
- `docs/standards/TOUCH_AND_RAISE_PATTERN.md`
- relevant files under `docs/domains/`
- relevant spec package under `specs/`

---

## 3) Reviewer

### Purpose
Evaluate correctness, change quality, risk, clarity, and standards compliance.

### Primary responsibility
Prevent weak, unclear, or undocumented changes from passing as acceptable delivery.

### Inputs
- diffs
- specs
- ADRs
- architecture and domain docs
- standards and governance rules

### Outputs
- review findings
- approval or change requests
- risk notes
- documentation drift findings
- standards compliance assessment

### Boundaries
- should not approve undocumented behavior changes
- should not treat stylistic preference as higher priority than correctness and clarity
- should not act as a substitute for validation or test execution

### When to use
- before merge
- before release readiness decisions
- after meaningful refactors
- when external contracts or multiple modules changed

### When not to use
- as a replacement for implementation planning
- as a substitute for automated validation

### Review rules
- compare the change against the intended depth
- check whether affected docs were updated
- look for silent contract drift
- identify missing tests or missing validation evidence
- prefer actionable review comments over vague criticism

### Consult first
- changed spec package in `specs/`
- relevant files in `docs/decisions/`
- relevant files in `docs/domains/`
- `docs/standards/CODING_STANDARDS.md`
- `docs/standards/DOC_UPDATE_POLICY.md`

---

## 4) Validator

### Purpose
Confirm that the change is ready from an execution, quality, and risk perspective.

### Primary responsibility
Provide a grounded go / no-go recommendation with visible residual risk.

### Inputs
- final change package
- test or verification evidence
- review findings
- rollout or release criteria
- risk prompts and standards

### Outputs
- validation summary
- pass / fail / conditional pass recommendation
- residual risk notes
- missing evidence list

### Boundaries
- must report uncertainty clearly
- must not claim readiness without evidence
- must not treat absence of evidence as evidence of correctness

### When to use
- after implementation
- before release or merge of meaningful changes
- before operational rollout
- when risk, impact, or ambiguity is high

### When not to use
- during early ideation
- when the task is still structurally undefined

### Validation rules
- validate observable behavior, not intent alone
- confirm that documentation and implementation do not drift silently
- check that assumptions were either resolved or explicitly recorded
- escalate to human review when risk exceeds confidence

### Consult first
- `docs/runbooks/RELEASE_CHECKLIST.md`
- relevant `review.md` and `validate.md` artifacts under `specs/`
- `docs/standards/TASK_DEPTH_POLICY.md`

---

## 5) Documentarian

### Purpose
Keep durable project memory synchronized with actual behavior, decisions, standards, and lessons.

### Primary responsibility
Ensure the repository remains understandable and trustworthy over time.

### Inputs
- implemented changes
- architecture shifts
- decisions made
- review findings
- lessons learned
- operational risks or gaps discovered

### Outputs
- updated docs
- updated specs
- ADRs when needed
- changelog entries
- lessons entries
- gap or discrepancy updates

### Boundaries
- should not alter technical behavior independently
- should not invent architecture or decisions not supported by evidence
- should not leave meaningful behavior changes undocumented

### When to use
- whenever behavior, architecture, standards, or process changed
- after incidents, migrations, or important reviews
- when new knowledge about legacy behavior is surfaced

### When not to use
- for truly no-op changes with no documentation impact

### Documentation rules
- treat `docs/` as durable operational memory
- treat `specs/` as the change package
- treat `prompts/` as reusable execution assets
- treat `docs/lessons/` as evolutionary memory
- prefer factual updates over aspirational prose

### Consult first
- `docs/standards/DOC_UPDATE_POLICY.md`
- `CHANGELOG.md`
- relevant files under `docs/architecture/`, `docs/domains/`, `docs/decisions/`, `docs/gaps/`, and `docs/lessons/`

---

## Default routing by task type

### Small local bug fix
- Primary: Implementer
- Support: Reviewer, Documentarian

### New feature in one area
- Primary: Orchestrator → Implementer
- Support: Reviewer, Documentarian

### Multi-module change or integration
- Primary: Orchestrator
- Support: Implementer, Reviewer, Validator, Documentarian

### Legacy hot spot change
- Primary: Orchestrator
- Support: Implementer, Reviewer, Documentarian
- Often requires Reverse depth artifacts

### Release or rollout decision
- Primary: Validator
- Support: Reviewer, Documentarian

---

## Final rule

If one person or one AI system is playing multiple roles, it must still preserve the separation of responsibilities.

Planning, implementation, review, validation, and documentation are distinct functions even when performed by the same actor.
