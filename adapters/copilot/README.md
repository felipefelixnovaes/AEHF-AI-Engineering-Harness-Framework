# Adapter Copilot

Este adapter explica como o AEHF é entregue em ambientes estilo GitHub Copilot.

O método AEHF não muda.
O que muda é como a memória do repositório e as regras de execução são disponibilizadas para a ferramenta.

---

## Propósito do adapter

O adapter Copilot existe para:
- fornecer um contrato operacional global estável
- delimitar orientações por contexto ou área de arquivo
- reutilizar arquivos de prompt como fluxos de trabalho operacionais
- reduzir ambiguidade sem sobrecarregar cada interação com contexto repetido

---

## Componentes do adapter

### 1. Regras globais
Arquivo:
- `.github/copilot-instructions.md`

Propósito:
- definir expectativas de comportamento em todo o repositório
- preservar o método AEHF no nível mais alto
- estabelecer regras para mudança, documentação, incerteza e validação

### 2. Regras delimitadas
Arquivos:
- `.github/instructions/*.instructions.md`

Propósito:
- fornecer orientações de comportamento mais específicas por caminho ou preocupação
- adaptar o framework a backend, frontend, docs, testes, migrações ou outros trabalhos delimitados
- evitar forçar um único arquivo de instrução grande a carregar o método inteiro

### 3. Prompts de execução reutilizáveis
Arquivos:
- `prompts/**/*.prompt.md`

Propósito:
- fornecer fluxos de trabalho reutilizáveis para cenários greenfield, brownfield, reverse, manutenção e governança
- reduzir prompting ad hoc e melhorar a repetibilidade

---

## Expectativas operacionais

Ao usar Copilot neste repositório, o comportamento esperado é:

- preservar o comportamento, a menos que a mudança seja intencional e documentada
- preferir mudanças incrementais em vez de reescrita
- classificar a profundidade da tarefa antes de criar artefatos
- usar `docs/` como fonte durável de verdade
- usar `specs/` como pacote de execução por mudança
- atualizar docs quando comportamento, arquitetura ou decisões mudarem
- tornar suposições explícitas
- escalar para validação humana quando o risco for alto

---

## Por que este adapter é estruturado desta forma

O Copilot funciona melhor quando o contexto é organizado em camadas em vez de despejado.

Este adapter, portanto, separa:
- regras universais do repositório
- orientações delimitadas por área
- fluxos de trabalho de execução reutilizáveis

Essa estrutura ajuda o framework a se manter:
- mais portátil
- mais fácil de manter
- menos repetitivo
- mais utilizável em diferentes tarefas

---

## Padrão de uso sugerido

Um fluxo de uso prático é:

1. ler as regras no nível do repositório em `.github/copilot-instructions.md`
2. aplicar qualquer arquivo de instrução delimitada relevante em `.github/instructions/`
3. escolher um fluxo de trabalho correspondente em `prompts/`
4. classificar a profundidade da tarefa usando `docs/standards/TASK_DEPTH_POLICY.md`
5. executar com base na memória do repositório em `docs/` e na estrutura do pacote de mudança em `specs/`

---

## O que este adapter não é

Este adapter não é:
- um substituto para o método AEHF
- uma licença para ignorar a memória do repositório
- um despejo gigante de instruções para toda situação
- um fork exclusivo do Copilot do framework

É simplesmente o mecanismo de entrega específico do Copilot para o mesmo modelo operacional universal AEHF.

---

## Regra final

Se as orientações específicas do Copilot conflitarem com a constituição ou os padrões centrais do AEHF, o método central prevalece.
