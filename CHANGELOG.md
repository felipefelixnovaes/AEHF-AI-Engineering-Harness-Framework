# Changelog

All notable changes to AEHF are documented in this file.

This project follows Keep a Changelog principles and semantic versioning intent.

---

## [0.1.0] - 2026-04-22

### Added

- Initial AEHF starter repository scaffold.
- Public launch-ready README and repository positioning.
- Core operational files: `AGENTS.md`, `CLAUDE.md`, `.github/copilot-instructions.md`, `CONTRIBUTING.md`, and `CHANGELOG.md`.
- Constitution, architecture model, standards, templates, runbooks, and example scenarios.
- Adaptive specs templates for Fast, Standard, Deep, and Reverse task depths.
- Reusable prompt library for greenfield, brownfield, reverse, maintenance, and governance workflows.
- Claude, Copilot, and generic adapter guidance.
- GitHub issue, PR, and instruction scaffolding for collaborative delivery.

### Defined

- AEHF as a universal framework for governed AI-assisted software delivery.
- The core operating principle: **minimum stable structure + depth on demand**.
- The five framework layers: Adaptive Specs, Project Memory, Execution Harness, Governance, and Evolution.
- The repository operating model where `docs/` is durable memory, `specs/` is the change package, `prompts/` is the execution library, and `docs/lessons/` is evolutionary memory.
- The task depth policy and routing model for Fast, Standard, Deep, and Reverse work.

### Standardized

- Documentation synchronization expectations through `DOC_UPDATE_POLICY.md`.
- Legacy modernization posture through `TOUCH_AND_RAISE_PATTERN.md`.
- Operational role separation through `AGENTS.md`.
- Tool-specific context delivery through Claude and Copilot adapters.

### Notes

This release establishes the AEHF core as a repository-first framework.
It is intentionally useful without requiring a CLI, hosted service, or runtime orchestration layer.
