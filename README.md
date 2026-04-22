# AI Engineering Harness Framework (AEHF)

**A production-grade, open-source meta-framework for governed AI-assisted software delivery.**

AEHF helps teams operationalize AI in software engineering without falling into either extreme:

- **chaotic vibe coding** (low consistency, weak memory, high rework)
- **heavy process bureaucracy** (slow delivery, high friction, low adoption)

AEHF’s operating principle is:

> **Minimum stable structure + depth on demand**

---

## Why AEHF exists

AI can accelerate coding, but many teams struggle to sustain quality over time. Context is lost, decisions drift, and delivery practices become inconsistent across contributors and tools.

AEHF provides a universal structure for:

- adaptive specs
- durable project memory
- execution control
- lightweight governance
- continuous framework evolution

It is intentionally **platform-agnostic** and not tied to Mission Control or any internal system.

---

## The 5 pillars

1. **Adaptive Specs Layer**  
   Match artifact depth to task complexity (Fast, Standard, Deep, Reverse).
2. **Project Memory Layer**  
   Treat docs as durable operational memory, not optional notes.
3. **Execution Harness Layer**  
   Guide model/workflow selection and reduce ambiguity and token waste.
4. **Governance Layer**  
   Keep quality with lightweight controls: ADRs, changelog, release checks, doc policy.
5. **Evolution Layer**  
   Expand safely over time (new adapters, tooling, runtime, hosted memory).

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

## Quick start

1. Clone this repository as your framework base.
2. Read `docs/constitution/CONSTITUTION.md`.
3. Choose your starting path:
   - **greenfield**: start from `prompts/greenfield/`
   - **brownfield**: start from `prompts/brownfield/`
4. Classify task depth using `docs/standards/TASK_DEPTH_POLICY.md`.
5. Create specs under `specs/` from the corresponding templates.
6. Execute changes and keep `docs/` updated per `DOC_UPDATE_POLICY.md`.

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
