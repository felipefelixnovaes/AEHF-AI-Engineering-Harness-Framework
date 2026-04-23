# Modelo de Repositório

O AEHF organiza os artefatos por finalidade e ciclo de vida:

- `docs/`: verdade de longa duração para arquitetura, padrões, operações e memória.
- `specs/`: pacote de mudança de nível de tarefa usado durante a entrega ativa.
- `prompts/`: instruções reutilizáveis para operações de AI repetíveis.
- `adapters/`: entrega de contexto específica por ferramenta sem alterar o método.
- `examples/`: referências de adoção para contextos organizacionais comuns.

## Separação de responsabilidades

- A memória operacional estável é separada do material de execução por tarefa.
- Os ativos de prompt são reutilizáveis e não estão vinculados a uma única implementação de projeto.
- As preocupações do adapter são isoladas para evitar o acoplamento método/ferramenta.
