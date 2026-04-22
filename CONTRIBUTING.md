# Contributing to AEHF

Thanks for contributing.

## Contribution principles

- Keep changes incremental and reviewable.
- Preserve existing behavior unless change is intentional and documented.
- Align every change with AEHF constitution and standards.
- Prefer clarity over novelty.

## Basic workflow

1. Open an issue or align on scope.
2. Classify task depth (`docs/standards/TASK_DEPTH_POLICY.md`).
3. Create/update specs from `specs/templates/`.
4. Implement in small slices.
5. Update docs per `docs/standards/DOC_UPDATE_POLICY.md`.
6. Add ADR when decision impact is architectural/process-significant.
7. Update `CHANGELOG.md` for notable changes.
8. Submit PR using `.github/pull_request_template.md`.

## Quality expectations

- No speculative rewrites.
- No undocumented behavior shifts.
- No orphan changes without memory updates.
- Prompt/library contributions must be reusable and outcome-oriented.

## Pull request acceptance criteria

- Scope is clear and bounded.
- Required artifacts are present for depth level.
- Docs/specs/code are synchronized.
- Risks and assumptions are explicit.
