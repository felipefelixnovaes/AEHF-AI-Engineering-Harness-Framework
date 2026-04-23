# CLAUDE Adapter Entry Point

Este repositório segue o AEHF.
Use este arquivo como um contrato operacional estrito ao trabalhar em ambientes no estilo Claude.

Seu propósito é fornecer um ponto de entrada curto e de alta prioridade para o método, a memória e as regras de execução do repositório.

---

## Leia primeiro

Siga esta ordem de leitura antes de propor mudanças não triviais:

1. `README.md`
2. `docs/constitution/CONSTITUTION.md`
3. `docs/architecture/INVENTORY.md`
4. `docs/standards/TASK_DEPTH_POLICY.md`
5. `docs/standards/CODING_STANDARDS.md`
6. `docs/standards/DOC_UPDATE_POLICY.md`
7. `AGENTS.md`

Se uma tarefa tocar um domínio específico ou pacote de spec, leia também:

- o arquivo relevante em `docs/domains/`
- o pacote de funcionalidade relevante em `specs/`
- decisões relacionadas em `docs/decisions/`
- lacunas relevantes em `docs/gaps/`

---

## Modelo do repositório

Trate o repositório como quatro camadas coordenadas:

- `docs/` = memória operacional durável e fonte da verdade
- `specs/` = pacote de execução por mudança
- `prompts/` = biblioteca de execução reutilizável
- `docs/lessons/` = memória evolutiva

Não trate a documentação como comentário opcional.
No AEHF, a documentação faz parte do sistema operacional da entrega.

---

## Regras operacionais obrigatórias

- Classificar a profundidade da tarefa antes de propor artefatos ou fluxo de trabalho.
- Preferir mudança incremental em vez de reescrita.
- Preservar o comportamento atual salvo se uma mudança intencional estiver explicitamente documentada.
- Usar padrões existentes antes de introduzir novos.
- Atualizar `docs/`, `specs/` e `CHANGELOG.md` quando comportamento, decisões, arquitetura ou padrões mudarem.
- Registrar premissas explicitamente.
- Não inventar certeza onde há evidências ausentes.
- Escalar para validação humana quando o risco ou a ambiguidade for alto.

---

## Modelo de profundidade de tarefas

Sempre classifique o trabalho usando `docs/standards/TASK_DEPTH_POLICY.md`.

Use:
- **Fast** para mudanças locais pequenas e de baixo risco
- **Standard** para mudanças normais de funcionalidade ou fluxo
- **Deep** para mudanças de alto risco, multi-módulo ou que afetam contratos
- **Reverse** para sistemas legados sem documentação confiável

A profundidade selecionada determina:
- quanto planejamento é necessário
- quais artefatos devem existir
- qual nível de validação é apropriado
- quanta governança é necessária

---

## Regras de comportamento de mudança

Ao fazer mudanças:

- preferir touch-and-raise em vez de reescrita especulativa
- preservar contratos externos salvo se a mudança de contrato for deliberada e documentada
- manter código, specs e docs sincronizados
- tornar a incerteza visível
- favorecer trade-offs explícitos em vez de desvio silencioso

Ao revisar ou raciocinar:

- distinguir fatos de premissas
- distinguir comportamento atual de comportamento pretendido
- distinguir verdade do repositório de preferência de ferramenta

---

## Regras de atualização de documentação

Quando o comportamento ou o entendimento mudar, atualize as fontes da verdade afetadas.
Isso pode incluir:

- `docs/architecture/`
- `docs/domains/`
- `docs/decisions/`
- `docs/gaps/`
- `docs/lessons/`
- `specs/`
- `CHANGELOG.md`

Não deixe a documentação desatualizada silenciosamente após mudanças significativas.

---

## Orientação de papéis

Use `AGENTS.md` para determinar a separação de papéis.
No mínimo, mantenha clareza entre:

- orquestração
- implementação
- revisão
- validação
- documentação

Um único ator pode desempenhar múltiplos papéis, mas as responsabilidades devem permanecer separadas.

---

## Postura padrão

Na dúvida:

- escolha o menor passo confiável
- preserve o comportamento
- torne as premissas explícitas
- atualize a memória do projeto
- prefira clareza a teatro de velocidade
