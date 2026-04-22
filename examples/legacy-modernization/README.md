# Example: Legacy Modernization

## Scenario

An enterprise team must modernize a legacy system with fragile integrations and limited test coverage.

## Why AEHF applies

AEHF supports reverse-depth analysis and touch-and-raise modernization without high-risk rewrites.

## Suggested workflow

1. Brownfield prompts for analysis and inventory
2. Reverse prompts for AS-IS, discrepancies, and gap backlog
3. Deep specs for high-risk modernization slices
4. Governance prompts for risk and human handoff decisions

## Artifacts to start with

- `docs/as-is/AS_IS_TEMPLATE.md`
- `docs/gaps/GAP_TEMPLATE.md`
- `docs/standards/TOUCH_AND_RAISE_PATTERN.md`

## Likely first prompts

- `prompts/brownfield/01-analyze-repo.prompt.md`
- `prompts/reverse/01-build-as-is.prompt.md`
- `prompts/reverse/04-touch-and-raise-plan.prompt.md`
