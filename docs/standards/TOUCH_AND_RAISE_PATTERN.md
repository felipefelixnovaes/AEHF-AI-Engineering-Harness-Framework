# Padrão Touch-and-Raise

Use este padrão para sistemas legados, brownfield ou parcialmente compreendidos.

Seu objetivo é melhorar a qualidade de uma área tocada sem desencadear um redesign injustificado ou desestabilizar uma reescrita ampla.

---

## Definição

Ao tocar um componente, eleve sua qualidade no lugar, preservando o menor escopo seguro possível.

Isso significa:
- corrigir o que deve ser corrigido
- melhorar o que diretamente reduz o risco atual
- documentar o que é descoberto
- adiar o redesign mais amplo para trabalho de acompanhamento explícito

Touch-and-raise é a postura padrão de modernização quando uma reescrita completa não está claramente justificada.

---

## Quando usar

Use este padrão quando:
- trabalhar em código legado
- tocar um ponto crítico com estrutura fraca
- alterar sistemas parcialmente compreendidos
- fazer progresso delimitado de modernização
- reduzir risco de forma incremental ao longo do tempo

É especialmente útil quando a entrega atual deve continuar enquanto a qualidade melhora gradualmente.

---

## Objetivos

O padrão existe para:
- preservar a continuidade da entrega
- reduzir o risco local imediato
- evitar grandes reescritas especulativas
- tornar cada área tocada ligeiramente mais fácil de entender e manter
- transformar o conhecimento descoberto em memória durável do repositório

---

## Regras fundamentais

### 1. Mantenha o escopo local
Mantenha a mudança ativa focada na área tocada e suas dependências diretas.
Não expanda para limpeza adjacente a menos que suporte diretamente a mudança atual.

### 2. Preserve o comportamento observável por padrão
Se o comportamento estiver sendo alterado intencionalmente, documente essa mudança explicitamente.
Não disfarce mudanças de comportamento como limpeza ou refatoração.

### 3. Melhore o que reduz o risco imediato
Boas melhorias de touch-and-raise incluem:
- nomenclatura mais clara
- funções menores ou estrutura mais clara
- limites mais seguros
- melhor validação ou testes
- remoção de duplicação óbvia na área tocada
- notas operacionais ou documentação de domínio mais claras

### 4. Registre o conhecimento oculto
Se você descobrir contratos implícitos, premissas, workarounds, restrições incomuns ou discrepâncias, registre-os na memória apropriada do repositório.

### 5. Adie o redesign amplo explicitamente
Se a área tocada revelar um problema estrutural maior, crie um item de backlog de acompanhamento, uma entrada de lacuna, um candidato a ADR ou um spec futuro.
Não contrabandear redesign em uma mudança local sem alinhamento.

---

## Fluxo de execução típico

1. identificar o menor escopo seguro
2. entender o comportamento observável atual
3. fazer a mudança necessária
4. melhorar a área tocada onde isso reduz diretamente o risco
5. adicionar ou fortalecer a validação em torno do comportamento tocado
6. documentar contratos, riscos ou restrições recém-descobertos
7. adiar o redesign maior para trabalho de acompanhamento explícito

---

## O que "raise" normalmente significa

Elevar a qualidade não significa embelezar tudo.
Normalmente significa uma ou mais das seguintes:

- o código é mais fácil de ler do que antes
- a estrutura local é menos frágil do que antes
- o comportamento é melhor protegido por testes ou validação
- a documentação é mais precisa do que antes
- o risco é mais visível do que antes
- os contratos ocultos são mais explícitos do que antes

Se nenhum desses aspectos melhorou, a parte de "raise" provavelmente não aconteceu.

---

## Anti-padrões

Evite:

- reescrita completa de subsistema sem evidências e alinhamento
- "limpeza" ampla não relacionada à mudança funcional
- misturar redesign arquitetural em uma correção de bug local sem justificativa explícita
- mudanças de comportamento não documentadas disfarçadas de refatoração
- tocar muitos arquivos não relacionados apenas por consistência estética
- assumir que a área tocada é totalmente compreendida porque uma mudança foi bem-sucedida

---

## Relação com a profundidade de tarefa

Touch-and-raise é frequentemente usado com:
- **Fast** para pequenas melhorias locais seguras
- **Standard** para modernização delimitada
- **Reverse** quando o comportamento atual deve ser reconstruído primeiro

É compatível com **Deep**, mas o trabalho Deep pode exigir planejamento mais amplo, validação mais rigorosa e decisões explícitas de arquitetura.

---

## Regra final

Deixe a área tocada mensuravelmente melhor do que você a encontrou, mas faça isso sem transformar uma mudança necessária em um redesign descontrolado.
