# AEHF Inventory

This file is the factual inventory of the AEHF repository.
It describes the framework's main layers, artifacts, adapters, workflows, and extension points.

Its purpose is to help contributors and AI tools understand what exists, what each part is for, and how the pieces fit together.

---

## 1. Framework layers

AEHF is organized around five core layers.

### 1. Adaptive Specs Layer
**Purpose:** Match process depth to task depth.

Primary artifacts:
- `docs/standards/TASK_DEPTH_POLICY.md`
- `specs/templates/*.template.md`
- `specs/` feature-level change packages

Core responsibility:
- prevent over-process for simple work
- prevent under-structuring for risky work

### 2. Project Memory Layer
**Purpose:** Preserve durable operational understanding.

Primary artifacts:
- `docs/architecture/`
- `docs/domains/`
- `docs/decisions/`
- `docs/gaps/`
- `docs/lessons/`
- `CHANGELOG.md`

Core responsibility:
- reduce repeated context dumping
- preserve architectural and domain understanding
- keep repository knowledge durable across sessions and contributors

### 3. Execution Harness Layer
**Purpose:** Structure how AI-assisted work is executed.

Primary artifacts:
- `prompts/`
- `AGENTS.md`
- `CLAUDE.md`
- `.github/copilot-instructions.md`
- `.github/instructions/`
- workflow docs and examples

Core responsibility:
- route work correctly
- reduce ambiguity
- align tool behavior with repository method

### 4. Governance Layer
**Purpose:** Keep delivery controlled without becoming bureaucratic.

Primary artifacts:
- `docs/constitution/CONSTITUTION.md`
- `docs/decisions/ADR_TEMPLATE.md`
- `docs/runbooks/RELEASE_CHECKLIST.md`
- `docs/standards/DOC_UPDATE_POLICY.md`
- `CHANGELOG.md`
- governance prompts under `prompts/governance/`

Core responsibility:
- preserve traceability
- surface risk
- maintain reviewability and change history

### 5. Evolution Layer
**Purpose:** Allow the framework to grow without breaking the core method.

Primary artifacts:
- `adapters/`
- `examples/`
- roadmap content in `README.md`
- future extension points documented here and elsewhere

Core responsibility:
- support new tools and delivery modes
- keep the method portable
- avoid lock-in to one ecosystem

---

## 2. Repository modules and responsibilities

### Top-level files

- `README.md` — launch document and primary framework entry point
- `CLAUDE.md` — Claude-style adapter entry point and operating contract
- `AGENTS.md` — role separation and execution routing model
- `CHANGELOG.md` — visible history of framework evolution
- `CONTRIBUTING.md` — contribution expectations and quality bar
- `LICENSE` — repository license

### `docs/`
Durable operational memory and source of truth.

Subareas include:
- `overview/` — framework explanation and adoption framing
- `constitution/` — non-negotiable principles
- `architecture/` — system model of the framework itself
- `domains/` — domain-level structures and templates
- `decisions/` — ADRs and decision records
- `as-is/` — current-state models for reverse or legacy contexts
- `to-be/` — desired target-state models
- `gaps/` — backlog of gaps, discrepancies, and risk items
- `standards/` — coding, documentation, and delivery rules
- `lessons/` — reusable learning and heuristics
- `runbooks/` — operational checklists and procedures

### `specs/`
Change packages and templates.

Purpose:
- capture intent
- plan execution
- structure validation
- improve reviewability

Subareas include:
- `templates/` — reusable spec templates by depth or artifact type
- feature folders — per-change packages containing `spec.md`, `plan.md`, `tasks.md`, `review.md`, and `validate.md` when appropriate

### `prompts/`
Reusable operational prompt library.

Purpose:
- provide repeatable workflows
- reduce prompt ambiguity
- support greenfield, brownfield, reverse, maintenance, and governance modes

Subareas include:
- `greenfield/`
- `brownfield/`
- `reverse/`
- `maintenance/`
- `governance/`

### `adapters/`
Tool-specific context delivery guidance.

Current modules:
- `adapters/claude/`
- `adapters/copilot/`
- `adapters/generic/`

Purpose:
- adapt the AEHF method to different AI tool ecosystems
- keep the method universal while varying context delivery

### `examples/`
Scenario-driven adoption starters.

Current scenarios:
- `greenfield-saas/`
- `legacy-modernization/`
- `enterprise-monorepo/`

Purpose:
- show how the framework applies in different repository realities
- reduce abstraction by giving concrete entry points

### `.github/`
GitHub-specific collaboration and Copilot integration area.

Includes:
- global Copilot instructions
- scoped instructions by area
- issue templates
- PR template

Purpose:
- improve contributor workflow
- align Copilot behavior with AEHF
- increase consistency in repository operations

---

## 3. Adapter entry points

Current adapter entry points are:

- Claude-style environments: `CLAUDE.md`
- GitHub Copilot environments: `.github/copilot-instructions.md`
- Generic tool alignment: `adapters/generic/README.md`

These adapters are delivery mechanisms, not alternate methods.
They should preserve the same AEHF principles while changing how context is consumed.

---

## 4. Current workflow families

AEHF currently supports the following workflow families:

### Greenfield
Used for new project or new subsystem setup.

Typical flow:
- bootstrap intent
- define architecture baseline
- map domains
- create feature specs
- implement with governance

### Brownfield
Used for existing repositories that need structure and stabilization.

Typical flow:
- analyze repository
- create inventory
- extract domains
- detect hotspots
- identify implicit standards

### Reverse
Used when current behavior must be reconstructed before safe change.

Typical flow:
- build as-is model
- identify discrepancies
- map gap backlog
- plan touch-and-raise path

### Maintenance
Used for continuous improvement and drift control.

Typical flow:
- update docs after change
- generate ADRs when needed
- review technical debt
- sync specs, code, and docs
- extract lessons

### Governance
Used for operating the method itself.

Typical flow:
- classify task depth
- assess risk
- choose model or workflow level
- decide human handoff
- assess release readiness

---

## 5. Known repository assumptions

This repository currently assumes:
- Markdown-first framework assets
- portability across Git-based repository platforms
- adapters as the primary mechanism for tool-specific integration
- no mandatory CLI or SaaS backend for core adoption

These assumptions may evolve, but the framework should remain useful in repository-only form.

---

## 6. Extension points

Planned extension points include:
- additional adapters for more AI tooling ecosystems
- optional CLI scaffolding
- optional IDE extension support
- optional runtime orchestration patterns
- optional hosted memory or telemetry services
- optional enterprise governance packs

All extension points must preserve:
- repository portability
- adapter separation
- method stability
- lightweight core adoption

---

## Final note

This inventory should remain factual.
It is not a roadmap pitch.
When the repository structure, responsibilities, or extension points change, update this file so it continues to reflect reality.
