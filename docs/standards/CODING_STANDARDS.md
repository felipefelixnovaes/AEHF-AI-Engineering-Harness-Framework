# Coding Standards

These standards are intentionally concise and universal.

## Core rules

- Preserve existing behavior unless a change is intentional and documented.
- Prefer incremental changes over broad rewrites.
- Keep changes scoped and reversible.
- Make assumptions explicit in specs/reviews.
- Keep tests and validation aligned with risk level.

## Legacy-sensitive changes

- Use touch-and-raise: improve only the touched area + immediate safety improvements.
- Avoid speculative architecture replacement.
- Document discovered constraints and hidden contracts.

## AI-assisted contribution rules

- Do not invent APIs or behavior without evidence.
- Verify generated changes against repository conventions.
- Update docs when behavior, interfaces, or operational flow changes.
