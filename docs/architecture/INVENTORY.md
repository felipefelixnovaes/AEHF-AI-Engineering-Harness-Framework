# AEHF Inventory

## Framework layers

1. Adaptive Specs Layer (`specs/`, `docs/standards/TASK_DEPTH_POLICY.md`)
2. Project Memory Layer (`docs/`, `docs/lessons/`, `CHANGELOG.md`)
3. Execution Harness Layer (`prompts/`, adapters, workflow model)
4. Governance Layer (ADRs, release/doc policies, risk prompts)
5. Evolution Layer (adapter + tooling extension points)

## Core modules and artifacts

- **Constitution:** `docs/constitution/CONSTITUTION.md`
- **Architecture models:** `docs/architecture/*.md`
- **Standards:** `docs/standards/*.md`
- **Decision records:** `docs/decisions/ADR_TEMPLATE.md`
- **Specs templates:** `specs/templates/*.template.md`
- **Prompt library:** `prompts/**/*.prompt.md`
- **Adapters:** `adapters/*/README.md`
- **Examples:** `examples/*/README.md`

## Adapters

- Claude adapter entry: `CLAUDE.md`
- Copilot adapter entry: `.github/copilot-instructions.md`
- Generic adapter contract: `adapters/generic/README.md`

## Workflows

- Greenfield bootstrap and feature delivery
- Brownfield analysis and stabilization
- Reverse modernization (as-is, gaps, touch-and-raise)
- Ongoing maintenance and governance checks

## Extension points (future)

- Additional adapter packages
- Optional CLI scaffolding
- IDE extensions (e.g., VS Code)
- Runtime orchestration patterns
- Hosted memory/index services

These extensions must not break core repository portability.
