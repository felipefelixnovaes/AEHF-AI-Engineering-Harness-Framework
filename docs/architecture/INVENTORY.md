# Inventário AEHF

Este arquivo é o inventário factual do repositório AEHF.
Descreve as principais camadas, artefatos, adapters, workflows e pontos de extensão do framework.

Seu objetivo é ajudar colaboradores e ferramentas de AI a entender o que existe, para que serve cada parte e como as peças se encaixam.

---

## 1. Camadas do framework

O AEHF é organizado em torno de cinco camadas centrais.

### 1. Camada de Specs Adaptativas
**Objetivo:** Alinhar a profundidade do processo à profundidade da tarefa.

Artefatos principais:
- `docs/standards/TASK_DEPTH_POLICY.md`
- `specs/templates/*.template.md`
- pacotes de mudança de nível de funcionalidade em `specs/`

Responsabilidade central:
- evitar excesso de processo para trabalhos simples
- evitar falta de estrutura para trabalhos arriscados

### 2. Camada de Memória do Projeto
**Objetivo:** Preservar o entendimento operacional durável.

Artefatos principais:
- `docs/architecture/`
- `docs/domains/`
- `docs/decisions/`
- `docs/gaps/`
- `docs/lessons/`
- `CHANGELOG.md`

Responsabilidade central:
- reduzir o despejo repetido de contexto
- preservar o entendimento de arquitetura e domínio
- manter o conhecimento do repositório durável entre sessões e colaboradores

### 3. Camada do Execution Harness
**Objetivo:** Estruturar como o trabalho assistido por AI é executado.

Artefatos principais:
- `prompts/`
- `AGENTS.md`
- `CLAUDE.md`
- `.github/copilot-instructions.md`
- `.github/instructions/`
- documentos de workflow e exemplos

Responsabilidade central:
- rotear o trabalho corretamente
- reduzir a ambiguidade
- alinhar o comportamento das ferramentas ao método do repositório

### 4. Camada de Governança
**Objetivo:** Manter a entrega controlada sem se tornar burocrática.

Artefatos principais:
- `docs/constitution/CONSTITUTION.md`
- `docs/decisions/ADR_TEMPLATE.md`
- `docs/runbooks/RELEASE_CHECKLIST.md`
- `docs/standards/DOC_UPDATE_POLICY.md`
- `CHANGELOG.md`
- prompts de governança em `prompts/governance/`

Responsabilidade central:
- preservar a rastreabilidade
- evidenciar o risco
- manter a revisabilidade e o histórico de mudanças

### 5. Camada de Evolução
**Objetivo:** Permitir que o framework cresça sem quebrar o método central.

Artefatos principais:
- `adapters/`
- `examples/`
- conteúdo de roadmap em `README.md`
- pontos de extensão futuros documentados aqui e em outros lugares

Responsabilidade central:
- suportar novas ferramentas e modos de entrega
- manter o método portável
- evitar lock-in em um único ecossistema

---

## 2. Módulos e responsabilidades do repositório

### Arquivos de nível superior

- `README.md` — documento de entrada e ponto de acesso principal ao framework
- `CLAUDE.md` — ponto de entrada do adapter estilo Claude e contrato de operação
- `AGENTS.md` — modelo de separação de papéis e roteamento de execução
- `CHANGELOG.md` — histórico visível da evolução do framework
- `CONTRIBUTING.md` — expectativas de contribuição e barra de qualidade
- `LICENSE` — licença do repositório

### `docs/`
Memória operacional durável e fonte de verdade.

Subáreas incluem:
- `overview/` — explicação do framework e enquadramento de adoção
- `constitution/` — princípios inegociáveis
- `architecture/` — modelo do sistema do próprio framework
- `domains/` — estruturas e templates de nível de domínio
- `decisions/` — ADRs e registros de decisão
- `as-is/` — modelos do estado atual para contextos reverse ou legados
- `to-be/` — modelos do estado-alvo desejado
- `gaps/` — backlog de lacunas, discrepâncias e itens de risco
- `standards/` — regras de codificação, documentação e entrega
- `lessons/` — aprendizados reutilizáveis e heurísticas
- `runbooks/` — checklists e procedimentos operacionais

### `specs/`
Pacotes de mudança e templates.

Objetivo:
- capturar a intenção
- planejar a execução
- estruturar a validação
- melhorar a revisabilidade

Subáreas incluem:
- `templates/` — templates de spec reutilizáveis por profundidade ou tipo de artefato
- pastas de funcionalidade — pacotes de mudança individuais contendo `spec.md`, `plan.md`, `tasks.md`, `review.md` e `validate.md` quando apropriado

### `prompts/`
Biblioteca operacional de prompts reutilizáveis.

Objetivo:
- fornecer workflows repetíveis
- reduzir a ambiguidade nos prompts
- suportar modos greenfield, brownfield, reverse, manutenção e governança

Subáreas incluem:
- `greenfield/`
- `brownfield/`
- `reverse/`
- `maintenance/`
- `governance/`

### `adapters/`
Orientações de entrega de contexto específicas por ferramenta.

Módulos atuais:
- `adapters/claude/`
- `adapters/copilot/`
- `adapters/generic/`

Objetivo:
- adaptar o método AEHF para diferentes ecossistemas de ferramentas de AI
- manter o método universal enquanto varia a entrega de contexto

### `examples/`
Pontos de entrada de adoção orientados a cenários.

Cenários atuais:
- `greenfield-saas/`
- `legacy-modernization/`
- `enterprise-monorepo/`

Objetivo:
- mostrar como o framework se aplica em diferentes realidades de repositório
- reduzir a abstração oferecendo pontos de entrada concretos

### `.github/`
Área de colaboração específica do GitHub e integração com Copilot.

Inclui:
- instruções globais do Copilot
- instruções com escopo por área
- templates de issue
- template de PR

Objetivo:
- melhorar o workflow dos colaboradores
- alinhar o comportamento do Copilot ao AEHF
- aumentar a consistência nas operações do repositório

---

## 3. Pontos de entrada dos adapters

Os pontos de entrada atuais dos adapters são:

- Ambientes estilo Claude: `CLAUDE.md`
- Ambientes GitHub Copilot: `.github/copilot-instructions.md`
- Alinhamento de ferramentas genéricas: `adapters/generic/README.md`

Esses adapters são mecanismos de entrega, não métodos alternativos.
Devem preservar os mesmos princípios AEHF enquanto mudam como o contexto é consumido.

---

## 4. Famílias de workflow atuais

O AEHF atualmente suporta as seguintes famílias de workflow:

### Greenfield
Usado para configuração de novo projeto ou novo subsistema.

Fluxo típico:
- inicializar a intenção
- definir a linha de base de arquitetura
- mapear domínios
- criar specs de funcionalidade
- implementar com governança

### Brownfield
Usado para repositórios existentes que precisam de estrutura e estabilização.

Fluxo típico:
- analisar o repositório
- criar inventário
- extrair domínios
- detectar pontos críticos
- identificar padrões implícitos

### Reverse
Usado quando o comportamento atual deve ser reconstruído antes de uma mudança segura.

Fluxo típico:
- construir o modelo as-is
- identificar discrepâncias
- mapear o backlog de lacunas
- planejar o caminho touch-and-raise

### Manutenção
Usado para melhoria contínua e controle de deriva.

Fluxo típico:
- atualizar docs após mudança
- gerar ADRs quando necessário
- revisar dívida técnica
- sincronizar specs, código e docs
- extrair lições

### Governança
Usado para operar o próprio método.

Fluxo típico:
- classificar a profundidade da tarefa
- avaliar o risco
- escolher o nível de modelo ou workflow
- decidir a transferência para humano
- avaliar a prontidão para release

---

## 5. Suposições conhecidas do repositório

Este repositório atualmente assume:
- ativos do framework baseados em Markdown
- portabilidade entre plataformas de repositório baseadas em Git
- adapters como mecanismo principal para integração específica por ferramenta
- nenhum CLI ou backend SaaS obrigatório para adoção central

Essas suposições podem evoluir, mas o framework deve permanecer útil apenas com o repositório.

---

## 6. Pontos de extensão

Os pontos de extensão planejados incluem:
- adapters adicionais para mais ecossistemas de ferramentas de AI
- scaffolding de CLI opcional
- suporte opcional a extensões de IDE
- padrões opcionais de orquestração em runtime
- serviços opcionais de memória hospedada ou telemetria
- pacotes opcionais de governança empresarial

Todos os pontos de extensão devem preservar:
- portabilidade do repositório
- separação de adapters
- estabilidade do método
- adoção central leve

---

## Nota final

Este inventário deve permanecer factual.
Não é um pitch de roadmap.
Quando a estrutura, as responsabilidades ou os pontos de extensão do repositório mudarem, atualize este arquivo para que continue refletindo a realidade.
