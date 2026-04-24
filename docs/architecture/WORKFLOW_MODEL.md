# Modelo de Workflow

## Fluxo padrão

1. Classificar a profundidade da tarefa.
2. Reunir os artefatos necessários.
3. Executar em fatias pequenas e verificáveis.
4. Validar o comportamento e o risco.
5. Sincronizar docs/specs/changelog.
6. Capturar lições quando relevante.

## Expectativas por profundidade

- **Fast:** artefatos mínimos, edições com escopo de baixo risco.
- **Standard:** rigor equilibrado para trabalhos comuns de funcionalidade/mudança.
- **Deep:** análise expandida, validação mais robusta e tratamento de risco.
- **Reverse:** entendimento da linha de base legada antes da transformação.

## Pontos de transferência

- Orquestrador -> Implementador: escopo aceito + lista de artefatos.
- Implementador -> Revisor: pacote de mudança completo.
- Revisor -> Validador: qualidade técnica aceita.
- Validador -> Documentarista: requisitos de atualização de memória prontos para release.
