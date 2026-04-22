# Context Delivery Model

## Core idea

All AI tools need context, but each consumes it differently. AEHF standardizes content and allows adapter-specific delivery.

## Context tiers

1. **Foundational context** (constitution + standards)
2. **Structural context** (architecture + domain maps)
3. **Task context** (specs + prompt selection)
4. **Validation context** (tests, risks, readiness)
5. **Memory updates** (docs/changelog/lessons)

## Delivery responsibilities

- Adapters define where context lives and how it is injected.
- Teams ensure required artifacts exist before execution.
- Orchestrator/Reviewer roles enforce context sufficiency.
