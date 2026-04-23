# Constituição AEHF

Esta constituição define os princípios inegociáveis do AEHF.

Esses princípios existem para manter a entrega de software assistida por AI rápida o suficiente para ser útil, estruturada o suficiente para ser confiável e flexível o suficiente para funcionar em diferentes ferramentas, equipes e tipos de repositório.

Se um workflow, prompt, adapter ou escolha de implementação entrar em conflito com esta constituição, a constituição prevalece.

---

## 1. Clareza acima da ambiguidade

Todo entregável significativo deve tornar explícitos o escopo, as suposições, os trade-offs e os resultados esperados.

Isso se aplica a:
- specs
- decisões de arquitetura
- mudanças de implementação
- resultados de revisão
- resultados de validação
- atualizações de documentação

Suposições ocultas geram dívida operacional.
Se algo é desconhecido, deve ser evidenciado claramente em vez de apenas insinuado.

---

## 2. Evolução incremental acima de reescrita

Prefira mudanças pequenas, reversíveis e compreensíveis a grandes reescritas.

A reescrita só é permitida quando justificada intencionalmente por evidências como:
- complexidade ou acoplamento inaceitáveis
- falha grave de manutenibilidade
- redesign de contrato
- restrições de migração que tornam a mudança incremental insegura ou ineficiente

A postura padrão é:
**touch-and-raise antes da reescrita**.

---

## 3. Memória estável acima de despejo repetido de contexto

`docs/` é a memória operacional durável.
O framework não deve depender de contexto de chat transitório, recordação humana ou repetição dispersa de prompts para permanecer compreensível.

Arquitetura, domínios, decisões, lacunas, padrões e lições devem ser preservados na memória do repositório.

Um sistema sólido deve se tornar mais fácil de raciocinar ao longo do tempo, não mais difícil.

---

## 4. Profundidade sob demanda acima de processo único para tudo

Nem toda mudança merece o mesmo ritual.

O AEHF exige que a profundidade da tarefa seja classificada antes de decidir quanta quantidade de processo, planejamento e governança é adequada.

O objetivo padrão é:
- estrutura suficiente para reduzir o risco
- não tanta estrutura que a entrega se transforme em burocracia

Fast, Standard, Deep e Reverse não são rótulos de prestígio.
São mecanismos de roteamento para escolher o menor modo operacional confiável.

---

## 5. Suposições explícitas acima de certeza alucinada

Incógnitas devem ser rotuladas como incógnitas.
Suposições devem ser declaradas como suposições.
Evidências devem ser distinguíveis de inferências.

O AEHF rejeita confiança falsa.
Uma resposta plausível não é suficiente; rastreabilidade importa.

Quando a certeza não está disponível:
- declare o que é conhecido
- declare o que é assumido
- declare o que deve ser validado

---

## 6. Sem divergência silenciosa entre código, specs e docs

Comportamento, specs, documentação de arquitetura e orientações operacionais não devem divergir silenciosamente.

Quando ocorre uma mudança significativa, as fontes de verdade correspondentes devem ser atualizadas.

Isso inclui mudanças em:
- comportamento observável
- entendimento de arquitetura
- regras de domínio
- padrões de entrega
- lacunas conhecidas
- decisões e trade-offs

Documentação silenciosamente desatualizada é uma falha de qualidade, não um problema cosmético.

---

## 7. Governança deve ser leve e acionável

A governança existe para melhorar a qualidade da entrega, não para criar teatro ritual.

O AEHF usa mecanismos leves como:
- ADRs
- atualizações de changelog
- artefatos de revisão
- artefatos de validação
- checklists de release
- prompts de risco

A governança deve responder perguntas reais de entrega:
- o que mudou
- por que mudou
- qual risco foi aceito
- o que ainda precisa de validação

Se a governança deixar de ser acionável, deve ser simplificada.

---

## 8. Adapters de ferramentas podem variar; o método permanece universal

Diferentes ferramentas de AI consomem contexto de formas distintas.
Isso é esperado.

Os adapters podem mudar como a memória do repositório é entregue, mas não devem alterar o método AEHF subjacente.

O método permanece constante entre as ferramentas:
- classificar a profundidade
- consultar a memória durável
- executar de forma incremental
- revisar e validar adequadamente
- atualizar a memória do projeto

Os adapters existem para melhorar a entrega de contexto, não para fragmentar o framework.

---

## 9. O repositório faz parte do sistema de execução

No AEHF, o repositório não é apenas um contêiner para código.
É um sistema operacional de entrega.

Isso significa:
- `docs/` carrega a memória durável
- `specs/` carrega a intenção de mudança e a estrutura de execução
- `prompts/` carrega workflows reutilizáveis
- `CHANGELOG.md` carrega a evolução visível
- adapters carregam a entrega de contexto específica de cada ferramenta

O próprio repositório deve ajudar a reduzir a ambiguidade, não amplificá-la.

---

## 10. O julgamento humano permanece parte do sistema

O AEHF foi projetado para entrega de software assistida por AI, não para automação cega.

A validação humana permanece necessária quando:
- o risco é alto
- a ambiguidade não está resolvida
- os contratos podem mudar
- o impacto no negócio é significativo
- as evidências são incompletas

A automação deve aumentar a alavancagem, não eliminar a responsabilidade.

---

## Regra final

O AEHF existe para criar progresso governado.

Em caso de dúvida, escolha o caminho que melhor preserva:
- clareza
- rastreabilidade
- confiabilidade incremental
- memória durável
- incerteza honesta
