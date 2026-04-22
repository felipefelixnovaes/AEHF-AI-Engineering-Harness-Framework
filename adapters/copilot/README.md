# Copilot Adapter

Copilot context delivery is split across repository and path-scoped instruction files.

## Adapter components

- Global rules: `.github/copilot-instructions.md`
- Scoped rules: `.github/instructions/*.instructions.md`
- Reusable execution prompts: `prompts/**/*.prompt.md`

## Operating expectations

- Preserve behavior unless intentional and documented.
- Prefer incremental changes over rewrites.
- Update docs when behavior or architecture changes.
- Classify task depth before creating artifacts.
