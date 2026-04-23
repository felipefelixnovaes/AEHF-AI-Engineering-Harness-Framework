# Modelo de Entrega de Contexto

## Ideia central

Todas as ferramentas de AI precisam de contexto, mas cada uma o consome de forma diferente. O AEHF padroniza o conteúdo e permite a entrega específica por adapter.

## Camadas de contexto

1. **Contexto fundacional** (constituição + padrões)
2. **Contexto estrutural** (arquitetura + mapas de domínio)
3. **Contexto de tarefa** (specs + seleção de prompt)
4. **Contexto de validação** (testes, riscos, prontidão)
5. **Atualizações de memória** (docs/changelog/lições)

## Responsabilidades de entrega

- Os adapters definem onde o contexto reside e como é injetado.
- As equipes garantem que os artefatos necessários existam antes da execução.
- Os papéis de Orquestrador/Revisor garantem a suficiência do contexto.
