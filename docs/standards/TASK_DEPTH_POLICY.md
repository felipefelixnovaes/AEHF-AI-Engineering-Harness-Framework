# Política de Profundidade de Tarefa

O AEHF suporta quatro profundidades de tarefa:

- Fast
- Standard
- Deep
- Reverse

O objetivo desta política é escolher o **menor nível confiável de processo** para uma tarefa.

Isso não é uma escada de maturidade nem um sistema de prestígio.
Um nível mais profundo não é automaticamente melhor.
O nível correto é aquele que corresponde ao risco, ambiguidade, escopo e reversibilidade.

---

## Regra fundamental

Sempre classifique a profundidade da tarefa antes de decidir:
- quais artefatos criar
- quanta planejamento é necessário
- quanta revisão é necessária
- quanta validação é necessária
- se é necessária escalada para validação humana

Se a profundidade selecionada for rasa demais, riscos importantes ficam sem gestão.
Se for profunda demais, o processo se torna desperdiçador e retarda a adoção.

---

## 1) Fast

### Quando usar
Use Fast para mudanças minúsculas, de baixo risco e altamente locais, onde o comportamento já é bem compreendido.

### Escopo típico
- correções de erros tipográficos
- alinhamento local de documentação
- edições menores de configuração
- correções de bugs muito pequenas e de baixo risco
- refatorações minúsculas sem impacto em contratos externos

### Características típicas
- toca uma pequena área
- baixa ambiguidade
- baixo raio de impacto
- fácil de revisar rapidamente
- fácil de validar diretamente

### Artefatos necessários
No mínimo:
- um pequeno spec ou nota de intenção
- uma lista de tarefas ou checklist de execução
- quaisquer atualizações de docs diretamente afetados

### Expectativa de revisão
- revisão leve
- confirmar que não há mudança silenciosa de comportamento
- confirmar que os docs ainda estão alinhados

### Expectativa de validação
- verificação observável direta
- testes leves ou evidências equivalentes

### Não use Fast quando
- múltiplos módulos estão envolvidos
- o comportamento externo pode mudar
- o comportamento legado não está claro
- a tarefa parece pequena mas tem acoplamento oculto

---

## 2) Standard

### Quando usar
Use Standard para trabalho normal de features, refatorações delimitadas e correções de impacto moderado onde o entendimento do repositório é razoavelmente confiável.

### Escopo típico
- uma feature em um subsistema
- uma mudança de fluxo delimitada
- uma refatoração moderada
- uma correção de bug normal com impacto visível para usuário ou sistema

### Características típicas
- impacto limitado mas significativo
- ambiguidade moderada
- um ou dois módulos ou domínios principais envolvidos
- revisão e validação normais necessárias

### Artefatos necessários
Tipicamente:
- `spec.md`
- `plan.md`
- `tasks.md`
- `review.md`
- `validate.md`

### Expectativa de revisão
- confirmar alinhamento com o comportamento pretendido
- verificar conformidade com padrões
- verificar alinhamento docs/spec/código
- identificar riscos ou lacunas ausentes

### Expectativa de validação
- testes adequados ou evidências equivalentes
- validação explícita do comportamento observável alterado

### Não use Standard quando
- o risco é materialmente alto
- arquitetura ou contratos estão mudando amplamente
- o comportamento atual não é bem compreendido
- a complexidade de migração é significativa

---

## 3) Deep

### Quando usar
Use Deep para trabalho de alto risco, transversal, alto custo ou que afeta contratos.

### Escopo típico
- refatorações arquiteturais
- mudanças críticas de confiabilidade ou segurança
- migrações entre módulos ou limites
- mudanças de modelo de dados ou interface
- entrega operacionalmente sensível

### Características típicas
- múltiplos módulos ou domínios envolvidos
- raio de impacto elevado
- custo de falha mais alto
- mais coordenação necessária
- governança e validação mais rigorosas necessárias

### Artefatos necessários
Tipicamente:
- `spec.md` detalhado
- `plan.md`
- `tasks.md`
- `review.md`
- `validate.md`
- notas de análise de risco
- considerações de rollout ou release
- ADRs quando decisões arquiteturais ou de política estão sendo tomadas

### Expectativa de revisão
- escrutínio mais rigoroso para arquitetura, contratos e estratégia de rollback
- identificação explícita de risco residual
- confirmação de que efeitos mais amplos no sistema foram considerados

### Expectativa de validação
- evidências mais sólidas
- testes ou verificação mais abrangentes
- avaliação explícita de prontidão
- validação humana se o risco permanecer alto

### Não use Deep quando
- a tarefa é verdadeiramente pequena e local
- o ritual extra não agregaria valor real de controle

---

## 4) Reverse

### Quando usar
Use Reverse para sistemas legados ou opacos onde o comportamento atual deve ser reconstruído antes que mudanças seguras possam ocorrer.

### Escopo típico
- modernização de módulos pouco documentados
- pontos críticos de alto risco com comportamento obscuro
- sistemas herdados com expectativas conflitantes
- áreas onde a equipe não possui um entendimento as-is confiável

### Características típicas
- incerteza é o principal risco
- o comportamento existente pode ser implícito ou contraditório
- documentação está ausente, desatualizada ou não é confiável
- mudança segura requer descoberta prévia

### Artefatos necessários
Tipicamente:
- `spec.md` Reverse
- artefatos as-is
- artefatos to-be quando apropriado
- análise de discrepâncias
- backlog de lacunas
- plano touch-and-raise

### Expectativa de revisão
- verificar se o comportamento atual foi distinguido do comportamento desejado
- verificar se as premissas foram tornadas explícitas
- verificar se lacunas e discrepâncias foram capturadas com honestidade

### Expectativa de validação
- validar o comportamento descoberto antes de depender dele
- confirmar que o caminho de mudança proposto preserva a segurança
- escalar quando o entendimento reconstruído ainda permanecer incerto

### Não use Reverse quando
- o comportamento atual já está claro e bem documentado
- a tarefa pode ser tratada com segurança usando Standard ou Deep

---

## Orientação de seleção

Escolha a menor profundidade que trate com segurança:
- incerteza
- impacto
- acoplamento
- reversibilidade
- carga de validação

Uma regra prática útil:
- se for minúsculo e óbvio, use **Fast**
- se for trabalho normal de produto ou engenharia, use **Standard**
- se for arriscado ou transversal, use **Deep**
- se o sistema atual não estiver claro, use **Reverse**

---

## Regras de escalada

Mova para um nível mais profundo quando qualquer um dos seguintes se tornar verdade:
- o escopo se expande além do limite original
- acoplamento oculto aparece
- o comportamento atual é menos compreendido do que o esperado
- a validação se torna mais complexa do que o esperado
- contratos externos podem mudar
- o risco é maior do que originalmente assumido

É aceitável começar em uma profundidade e escalar depois.
Não é aceitável permanecer raso depois que o quadro de risco muda.

---

## Regra final

A profundidade de tarefa é um mecanismo de controle.
Use-a para manter a entrega proporcional, revisável e confiável.

O AEHF funciona melhor quando o processo não é nem muito leve nem muito pesado, mas compatível com a realidade.
