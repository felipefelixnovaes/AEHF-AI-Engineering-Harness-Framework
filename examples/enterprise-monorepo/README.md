# Example: Enterprise Monorepo

## Scenario

Multiple teams share a large monorepo with varied maturity and strict governance needs.

## Why AEHF applies

AEHF offers common standards and adaptive depth so teams align without forcing one rigid process.

## Suggested workflow

1. Define domain maps and ownership boundaries
2. Apply Standard depth by default, Deep for cross-cutting changes
3. Use governance prompts for risk gating and release readiness
4. Capture ADRs and lessons continuously

## Artifacts to start with

- `docs/architecture/INVENTORY.md`
- `docs/domains/DOMAIN_TEMPLATE.md`
- `docs/standards/TASK_DEPTH_POLICY.md`

## Likely first prompts

- `prompts/brownfield/02-create-inventory.prompt.md`
- `prompts/governance/01-classify-task-depth.prompt.md`
- `prompts/governance/05-release-readiness.prompt.md`
