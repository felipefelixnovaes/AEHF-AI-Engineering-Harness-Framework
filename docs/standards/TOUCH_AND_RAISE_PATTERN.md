# Touch-and-Raise Pattern

Use this pattern for legacy/brownfield systems.

## Definition

When touching a component, raise its quality in-place without triggering broad rewrites.

## Rules

- Keep scope local to the changed area and direct dependencies.
- Add tests/validation around touched behavior.
- Improve naming, structure, and docs where it reduces immediate risk.
- Record hidden contracts and constraints discovered during change.
- Defer large redesign into explicit follow-up backlog items.

## Anti-patterns

- full subsystem rewrite without baseline evidence
- broad “cleanup” commits unrelated to functional change
- undocumented behavior changes disguised as refactor
