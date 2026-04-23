# AI Engineering Harness Framework (AEHF)

> 🇧🇷 Leia em Português (Brasil): [README.pt-BR.md](README.pt-BR.md)

**Stop vibe coding. Start governed AI engineering.**

AEHF is an open-source framework for AI-assisted software delivery.
It helps teams move faster without losing structure, and add control without creating heavyweight process.

AEHF is built for the space between two broken extremes:

- **chaotic vibe coding** — fast output, weak memory, inconsistent quality, high rework
- **heavy process bureaucracy** — rigid rituals, slow delivery, poor adoption, wasted effort

Its core operating principle is:

> **Minimum stable structure + depth on demand**

---

## Core idea

**AEHF gives AI a stable engineering harness: enough structure to stay reliable, enough flexibility to stay fast.**

---

## Why AEHF exists

AI can generate code quickly, but speed alone does not create reliable software delivery.

In real projects, teams run into the same problems repeatedly:

- context gets lost between sessions and contributors
- implementation drifts away from documentation
- legacy systems remain poorly understood
- change depth is not matched to process depth
- every tool invents its own workflow
- prompts become operational debt

AEHF provides a universal operational model for AI-assisted software engineering through:

- adaptive specs
- durable project memory
- execution control
- lightweight governance
- continuous evolution

It is intentionally **platform-agnostic** and not tied to Mission Control or any internal system.

---

## What AEHF is

- a framework for governed AI-assisted software delivery
- a repository operating model for AI engineering
- a durable documentation and memory structure
- a tool-adapter friendly method that works across ecosystems

## What AEHF is not

- a replacement for LLMs
- a multi-agent runtime by default
- a heavy enterprise process suite
- an app generator disguised as a framework

---

## The 5 pillars

1. **Adaptive Specs**  
   Use the right level of rigor for the task: Fast, Standard, Deep, or Reverse.
2. **Project Memory**  
   Keep architecture, decisions, domains, gaps, and lessons as durable operational memory.
3. **Execution Harness**  
   Guide which model, workflow, and validation path to use based on risk and cost.
4. **Lightweight Governance**  
   Keep control through ADRs, changelogs, release checks, and documentation policy.
5. **Built-in Evolution**  
   Expand safely across new tools, adapters, and operating models without breaking the core method.

---

## Why AEHF improves AI engineering

AEHF improves real-world AI delivery by reducing:

- ambiguous prompts
- repeated context dumping
- undocumented assumptions
- workflow drift between contributors
- silent divergence between code and docs

And it improves:

- consistency
- reviewability
- onboarding
- maintainability
- cost efficiency

---

## Who this is for

- solo developers
- startups
- software factories
- enterprise delivery teams
- teams modernizing legacy systems

---

## Repository structure

```text
README.md                    # launch guide and framework entry point
CLAUDE.md                    # strict adapter entry point for Claude-style agents
AGENTS.md                    # operational agent roles and boundaries
CHANGELOG.md                 # framework evolution log
CONTRIBUTING.md              # contribution workflow and quality bar

docs/                        # durable operational memory (source of truth)
specs/                       # per-change execution package and templates
prompts/                     # reusable operational prompt library
adapters/                    # tool-specific context delivery guidance
examples/                    # scenario-driven adoption starters
.github/                     # copilot instructions, issue/PR templates
```

---

## Get value in 15 minutes

- Use `prompts/greenfield/` to start a new project with structure.
- Use `prompts/brownfield/` to map and stabilize a legacy repository.
- Use `docs/standards/TASK_DEPTH_POLICY.md` to classify work.
- Use `specs/templates/` to package change safely.
- Use adapters to deliver context to your AI tool of choice.

---

## Quick start

1. Clone this repository as your framework base.
2. Read `docs/constitution/CONSTITUTION.md`.
3. Choose your starting path:
   - **greenfield**: start from `prompts/greenfield/`
   - **brownfield**: start from `prompts/brownfield/`
4. Classify task depth using `docs/standards/TASK_DEPTH_POLICY.md`.
5. Create specs under `specs/` from the corresponding templates.
6. Execute changes and keep `docs/` updated per `docs/standards/DOC_UPDATE_POLICY.md`.

---

## Greenfield workflow (suggested)

1. Bootstrap project intent and constraints (`01-bootstrap-project`).
2. Draft initial architecture (`02-first-architecture`).
3. Create domain map (`03-create-domain-map`).
4. Build feature spec (`04-create-feature-spec`).
5. Implement iteratively with governance checks (`05-implement-feature`).

Artifacts to prioritize:

- `specs/templates/standard-spec.template.md`
- `docs/architecture/REPOSITORY_MODEL.md`
- `docs/domains/DOMAIN_TEMPLATE.md`
- `docs/decisions/ADR_TEMPLATE.md`

---

## Brownfield workflow (suggested)

1. Analyze existing repository and constraints (`01-analyze-repo`).
2. Build current-state inventory (`02-create-inventory`).
3. Extract implicit domains (`03-extract-domains`).
4. Detect hotspots and operational risk (`04-detect-hotspots`).
5. Surface implicit standards (`05-map-implicit-standards`).

For modernization planning, continue with `prompts/reverse/`.

---

## Adapter model

AEHF method is universal; **context delivery is adapter-specific**.

- **Claude adapter**: `CLAUDE.md` is the strict memory entry point.
- **Copilot adapter**:
  - global rules in `.github/copilot-instructions.md`
  - scoped rules in `.github/instructions/*.instructions.md`
  - reusable prompt operations in `prompts/*.prompt.md`
- **Generic adapter**: documented in `adapters/generic/README.md`.

---

## Roadmap

### v0.2

- richer prompt variants for testing and migration scenarios
- additional example playbooks for regulated environments
- stronger cross-links across docs/specs/prompts

### v1.0

- adapter expansion for additional AI tooling ecosystems
- optional CLI scaffolding without coupling core method
- optional telemetry/dashboard patterns for governance insights

---

## Contributing

See `CONTRIBUTING.md` for contribution flow, quality standards, and review expectations.

If you change behavior, update docs/specs/changelog in the same change package.

---

## License

MIT — see `LICENSE`.
