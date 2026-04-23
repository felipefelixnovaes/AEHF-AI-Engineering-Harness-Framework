# AEHF Operational Agents

Este arquivo define os papéis de execução do AEHF para entrega de software assistida por AI.
São **papéis operacionais**, não personalidades.

Seu propósito é reduzir ambiguidades, separar responsabilidades e melhorar as transições entre planejamento, execução, revisão, validação e documentação.

## Como usar este arquivo

Use esses papéis como um modelo de roteamento para o trabalho.
Uma única pessoa ou assistente de AI pode desempenhar múltiplos papéis, mas as responsabilidades devem permanecer distintas.

Antes de iniciar o trabalho:

1. classificar a profundidade da tarefa
2. identificar o papel principal que conduz a tarefa
3. identificar quais papéis de suporte são necessários
4. definir os artefatos que devem ser consultados ou atualizados

---

## 1) Orchestrator

### Propósito
Planejar o trabalho, classificar a profundidade, selecionar o fluxo de trabalho correto e rotear tarefas para o papel adequado.

### Responsabilidade principal
Transformar uma solicitação recebida em um caminho de execução governado.

### Entradas
- solicitação de tarefa
- restrições e critérios de sucesso
- estado atual do repositório
- contexto de arquitetura e domínio
- documentos de padrões e governança

### Saídas
- profundidade de tarefa escolhida
- recomendação de fluxo de trabalho
- plano de artefatos
- plano de atribuição de papéis ou de transição
- premissas explícitas e questões em aberto

### Limites
- não realiza trabalho de implementação extenso diretamente, salvo se a tarefa for trivial
- não deve pular a classificação de profundidade
- não deve inventar contexto ausente sem rotulá-lo como premissa

### Quando usar
- no início de qualquer tarefa não trivial
- quando o fluxo de trabalho correto não está claro
- quando múltiplos módulos ou artefatos estão envolvidos
- ao equilibrar velocidade, custo e risco

### Quando não usar
- para edições locais minúsculas sem impacto de coordenação ou documentação

### Consultar primeiro
- `README.md`
- `docs/constitution/CONSTITUTION.md`
- `docs/standards/TASK_DEPTH_POLICY.md`
- `docs/architecture/INVENTORY.md`

---

## 2) Implementer

### Propósito
Executar incrementalmente alterações aprovadas de código, documentação, spec ou configuração.

### Responsabilidade principal
Produzir mudanças corretas e rastreáveis que respeitem o fluxo de trabalho escolhido e os padrões do repositório.

### Entradas
- artefatos de spec
- plano aceito
- docs de arquitetura e domínio
- padrões de codificação e documentação
- padrões de implementação existentes

### Saídas
- mudanças funcionais
- artefatos atualizados
- notas de implementação quando necessário
- diffs rastreáveis prontos para commit

### Limites
- não deve contornar regras de governança
- não deve reescrever amplamente quando existe um caminho incremental
- não deve introduzir novos padrões sem verificar as convenções existentes
- não deve alterar silenciosamente o comportamento externo

### Quando usar
- implementação de funcionalidades
- correções de bugs
- refatorações
- fatias de migração
- mudanças alinhadas à documentação

### Quando não usar
- aprovação independente de qualidade
- aprovação de arquitetura
- decisões de prontidão para lançamento

### Regras de execução
- preferir touch-and-raise em vez de reescrita
- preservar o comportamento salvo se a mudança intencional estiver documentada
- atualizar os docs tocados quando comportamento, estrutura ou decisões mudarem
- sinalizar incerteza em vez de adivinhar

### Consultar primeiro
- `docs/standards/CODING_STANDARDS.md`
- `docs/standards/DOC_UPDATE_POLICY.md`
- `docs/standards/TOUCH_AND_RAISE_PATTERN.md`
- arquivos relevantes em `docs/domains/`
- pacote de spec relevante em `specs/`

---

## 3) Reviewer

### Propósito
Avaliar correção, qualidade da mudança, risco, clareza e conformidade com padrões.

### Responsabilidade principal
Impedir que mudanças fracas, pouco claras ou não documentadas sejam aceitas como entrega adequada.

### Entradas
- diffs
- specs
- ADRs
- docs de arquitetura e domínio
- regras de padrões e governança

### Saídas
- descobertas da revisão
- aprovação ou solicitações de mudança
- notas de risco
- descobertas de desvio de documentação
- avaliação de conformidade com padrões

### Limites
- não deve aprovar mudanças de comportamento não documentadas
- não deve tratar preferência estilística como prioridade maior do que correção e clareza
- não deve agir como substituto para validação ou execução de testes

### Quando usar
- antes do merge
- antes de decisões de prontidão para lançamento
- após refatorações significativas
- quando contratos externos ou múltiplos módulos foram alterados

### Quando não usar
- como substituto para planejamento de implementação
- como substituto para validação automatizada

### Regras de revisão
- comparar a mudança com a profundidade pretendida
- verificar se os docs afetados foram atualizados
- identificar desvio silencioso de contratos
- identificar testes ausentes ou evidências de validação ausentes
- preferir comentários de revisão acionáveis a críticas vagas

### Consultar primeiro
- pacote de spec alterado em `specs/`
- arquivos relevantes em `docs/decisions/`
- arquivos relevantes em `docs/domains/`
- `docs/standards/CODING_STANDARDS.md`
- `docs/standards/DOC_UPDATE_POLICY.md`

---

## 4) Validator

### Propósito
Confirmar que a mudança está pronta do ponto de vista de execução, qualidade e risco.

### Responsabilidade principal
Fornecer uma recomendação fundamentada de prosseguir / não prosseguir com o risco residual visível.

### Entradas
- pacote final de mudança
- evidências de teste ou verificação
- descobertas da revisão
- critérios de lançamento ou rollout
- prompts de risco e padrões

### Saídas
- resumo de validação
- recomendação de aprovação / reprovação / aprovação condicional
- notas de risco residual
- lista de evidências ausentes

### Limites
- deve relatar incerteza claramente
- não deve afirmar prontidão sem evidências
- não deve tratar ausência de evidência como evidência de correção

### Quando usar
- após a implementação
- antes do lançamento ou merge de mudanças significativas
- antes do rollout operacional
- quando risco, impacto ou ambiguidade é alto

### Quando não usar
- durante a idealização inicial
- quando a tarefa ainda está estruturalmente indefinida

### Regras de validação
- validar comportamento observável, não apenas intenção
- confirmar que documentação e implementação não divergem silenciosamente
- verificar se as premissas foram resolvidas ou explicitamente registradas
- escalar para revisão humana quando o risco superar a confiança

### Consultar primeiro
- `docs/runbooks/RELEASE_CHECKLIST.md`
- artefatos `review.md` e `validate.md` relevantes em `specs/`
- `docs/standards/TASK_DEPTH_POLICY.md`

---

## 5) Documentarian

### Propósito
Manter a memória durável do projeto sincronizada com o comportamento real, decisões, padrões e lições aprendidas.

### Responsabilidade principal
Garantir que o repositório permaneça compreensível e confiável ao longo do tempo.

### Entradas
- mudanças implementadas
- mudanças de arquitetura
- decisões tomadas
- descobertas da revisão
- lições aprendidas
- riscos operacionais ou lacunas descobertas

### Saídas
- docs atualizados
- specs atualizados
- ADRs quando necessário
- entradas de changelog
- entradas de lições
- atualizações de lacunas ou discrepâncias

### Limites
- não deve alterar o comportamento técnico de forma independente
- não deve inventar arquitetura ou decisões sem suporte de evidências
- não deve deixar mudanças de comportamento significativas sem documentação

### Quando usar
- sempre que comportamento, arquitetura, padrões ou processo mudarem
- após incidentes, migrações ou revisões importantes
- quando novo conhecimento sobre comportamento legado for revelado

### Quando não usar
- para mudanças verdadeiramente sem efeito e sem impacto na documentação

### Regras de documentação
- tratar `docs/` como memória operacional durável
- tratar `specs/` como o pacote de mudança
- tratar `prompts/` como ativos de execução reutilizáveis
- tratar `docs/lessons/` como memória evolutiva
- preferir atualizações factuais a prosa aspiracional

### Consultar primeiro
- `docs/standards/DOC_UPDATE_POLICY.md`
- `CHANGELOG.md`
- arquivos relevantes em `docs/architecture/`, `docs/domains/`, `docs/decisions/`, `docs/gaps/` e `docs/lessons/`

---

## Roteamento padrão por tipo de tarefa

### Correção local de bug pequeno
- Principal: Implementer
- Suporte: Reviewer, Documentarian

### Nova funcionalidade em uma área
- Principal: Orchestrator → Implementer
- Suporte: Reviewer, Documentarian

### Mudança ou integração multi-módulo
- Principal: Orchestrator
- Suporte: Implementer, Reviewer, Validator, Documentarian

### Mudança em ponto crítico legado
- Principal: Orchestrator
- Suporte: Implementer, Reviewer, Documentarian
- Frequentemente requer artefatos de profundidade Reverse

### Decisão de lançamento ou rollout
- Principal: Validator
- Suporte: Reviewer, Documentarian

---

## Regra final

Se uma pessoa ou um sistema de AI está desempenhando múltiplos papéis, ainda assim deve preservar a separação de responsabilidades.

Planejamento, implementação, revisão, validação e documentação são funções distintas, mesmo quando realizadas pelo mesmo ator.
