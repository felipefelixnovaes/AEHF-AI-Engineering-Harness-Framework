# Repository Model

AEHF organizes artifacts by purpose and lifecycle:

- `docs/`: long-lived truth for architecture, standards, operations, and memory.
- `specs/`: task-level change package used during active delivery.
- `prompts/`: reusable instructions for repeatable AI operations.
- `adapters/`: tool-specific context delivery without changing method.
- `examples/`: adoption references for common organizational contexts.

## Separation of concerns

- Stable operational memory is separated from per-task execution material.
- Prompt assets are reusable and not tied to a single project implementation.
- Adapter concerns are isolated to prevent method/tool coupling.
