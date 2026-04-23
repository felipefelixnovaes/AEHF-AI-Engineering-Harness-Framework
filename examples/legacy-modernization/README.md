# Exemplo: Modernização de Sistema Legado

## Cenário

Uma equipe corporativa precisa modernizar um sistema legado com integrações frágeis e cobertura de testes limitada.

## Por que o AEHF se aplica

O AEHF suporta análise de profundidade Reverse e modernização touch-and-raise sem reescritas de alto risco.

## Fluxo de trabalho sugerido

1. Prompts brownfield para análise e inventário
2. Prompts reverse para AS-IS, discrepâncias e backlog de lacunas
3. Specs Deep para fatias de modernização de alto risco
4. Prompts de governança para decisões de risco e handoff humano

## Artefatos para começar

- `docs/as-is/AS_IS_TEMPLATE.md`
- `docs/gaps/GAP_TEMPLATE.md`
- `docs/standards/TOUCH_AND_RAISE_PATTERN.md`

## Primeiros prompts prováveis

- `prompts/brownfield/01-analyze-repo.prompt.md`
- `prompts/reverse/01-build-as-is.prompt.md`
- `prompts/reverse/04-touch-and-raise-plan.prompt.md`
