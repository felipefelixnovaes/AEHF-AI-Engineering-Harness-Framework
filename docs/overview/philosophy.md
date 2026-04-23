# Filosofia AEHF

## Estrutura mínima estável + profundidade sob demanda

O AEHF é construído sobre uma convicção simples:
a entrega de software com AI precisa de estrutura, mas não da quantidade errada de estrutura.

O framework evita intencionalmente dois extremos prejudiciais:

1. **sem estrutura** — alta entropia, memória fraca, baixa repetibilidade
2. **processo máximo** — alto atrito, baixa adoção, entrega lenta

A abordagem do AEHF é manter um núcleo estável pequeno e escalar o rigor proporcionalmente à realidade da tarefa.

---

## O que isso significa na prática

### Comece com o núcleo mínimo estável
Todo projeto deve ter estrutura suficiente para permanecer compreensível e governável.
No mínimo, isso significa:
- memória de projeto durável
- seleção explícita de profundidade de tarefa
- padrões de execução reutilizáveis
- governança leve
- o hábito de manter docs e código alinhados

### Adicione profundidade somente quando a realidade exigir
Não force specs ou processos pesados para toda mudança.
Aumente o rigor quando:
- o risco for maior
- o escopo for mais amplo
- os contratos puderem mudar
- o comportamento legado for obscuro
- o esforço de validação for maior

### Mantenha a memória durável
Não dependa de explicações repetidas em prompts ou de contexto humano transitório.
Use o próprio repositório para preservar o entendimento ao longo do tempo.

### Mantenha as mudanças incrementais
Prefira progresso pequeno e revisável a grande reinvenção.
O AEHF favorece a evolução controlada em vez do reinício dramático.

### Mantenha a incerteza honesta
O framework parte do princípio de que a ambiguidade existe.
Seu papel não é fingir que a incerteza não existe, mas contê-la por meio de estrutura, visibilidade e validação.

---

## A filosofia por trás das camadas

As camadas do AEHF não são categorias arbitrárias.
Elas refletem pontos de falha recorrentes na entrega de software assistida por AI:

- o trabalho falha quando as specs não correspondem ao risco
- o trabalho falha quando a memória do projeto é fraca
- o trabalho falha quando a execução não é roteada corretamente
- o trabalho falha quando a governança está ausente ou é excessiva
- o trabalho falha quando o sistema não consegue evoluir sem recomeçar do zero

O framework existe para estabilizar esses pontos de falha.

---

## Postura de design

O AEHF prefere:
- clareza a novidade
- processo proporcional a ritual indiscriminado
- suposições explícitas a suposições ocultas
- touch-and-raise a reescrita especulativa
- memória do repositório a despejo repetido de contexto
- progresso governado a ambiguidade veloz

---

## Princípio final

O AEHF não está tentando maximizar o processo.
Está tentando maximizar o progresso confiável.

O objetivo não é fazer a AI parecer poderosa.
O objetivo é fazer a entrega assistida por AI permanecer útil ao longo do tempo.
