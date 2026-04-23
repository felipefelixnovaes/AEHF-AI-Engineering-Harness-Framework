# Exemplo: Monorepo Corporativo

## Cenário

Múltiplas equipes compartilham um grande monorepo com maturidade variada e necessidades rígidas de governança.

## Por que o AEHF se aplica

O AEHF oferece padrões comuns e profundidade adaptativa para que as equipes se alinhem sem impor um processo rígido único.

## Fluxo de trabalho sugerido

1. Definir mapas de domínio e limites de responsabilidade
2. Aplicar profundidade Standard por padrão, Deep para mudanças transversais
3. Usar prompts de governança para gate de risco e prontidão de release
4. Capturar ADRs e lições continuamente

## Artefatos para começar

- `docs/architecture/INVENTORY.md`
- `docs/domains/DOMAIN_TEMPLATE.md`
- `docs/standards/TASK_DEPTH_POLICY.md`

## Primeiros prompts prováveis

- `prompts/brownfield/02-create-inventory.prompt.md`
- `prompts/governance/01-classify-task-depth.prompt.md`
- `prompts/governance/05-release-readiness.prompt.md`
