# Instruções do Repositório Copilot (AEHF)

Este repositório segue o AEHF.
Estas instruções definem como o GitHub Copilot deve se comportar ao assistir neste repositório.

O objetivo não é apenas gerar saída, mas preservar um método de entrega governado em código, documentação, specs e memória do repositório.

---

## Modelo operacional do repositório

Trate o repositório como quatro camadas coordenadas:

- `docs/` é a fonte durável da verdade
- `specs/` é o pacote de execução por mudança
- `prompts/` é a biblioteca operacional de prompts reutilizáveis
- `docs/lessons/` é a camada de memória evolutiva

Não trate a documentação como secundária.
Neste repositório, memória durável faz parte da qualidade de entrega.

---

## Comportamento obrigatório

Sempre:

- preservar o comportamento existente salvo se uma mudança for intencional e documentada
- preferir mudança incremental em vez de reescrita
- classificar a profundidade da tarefa antes de propor artefatos ou fluxo de trabalho
- usar as convenções existentes do repositório antes de introduzir novos padrões
- atualizar docs, specs e changelog quando comportamento, arquitetura, decisões ou padrões mudarem
- tornar premissas explícitas
- distinguir fatos de premissas
- escalar para validação humana quando o risco ou a ambiguidade for alto

Nunca:

- reescrever amplamente sem justificativa
- alterar silenciosamente contratos externos
- deixar desvio significativo de documentação para trás
- apresentar incerteza como certeza

---

## Regras de profundidade de tarefas

Use `docs/standards/TASK_DEPTH_POLICY.md` antes de decidir quanto processo ou quantos artefatos são necessários.

Níveis de profundidade:

- **Fast**: mudança pequena, de baixo risco e local
- **Standard**: mudança normal de funcionalidade ou fluxo
- **Deep**: mudança de alto risco, entre módulos, de migração ou com impacto em contratos
- **Reverse**: sistema legado ou mal documentado onde o comportamento atual deve ser reconstruído

A profundidade selecionada deve influenciar:

- rigor de planejamento
- criação de artefatos
- expectativas de revisão
- necessidades de validação
- escopo de documentação

---

## Regras de entrega

Ao implementar:

- verificar `docs/architecture/INVENTORY.md`
- verificar arquivos de domínio relevantes em `docs/domains/`
- verificar decisões relevantes em `docs/decisions/`
- verificar lacunas abertas relevantes em `docs/gaps/`
- atualizar as fontes da verdade afetadas quando o comportamento ou o entendimento mudar

Ao tocar código legado:

- preferir touch-and-raise em vez de reescrita
- preservar o comportamento observável salvo se estiver sendo mudado intencionalmente
- documentar comportamento recém-descoberto
- registrar discrepâncias e lacunas quando o comportamento atual conflitar com o esperado

Ao atualizar docs:

- preferir atualizações factuais e duráveis em vez de prosa aspiracional
- manter código, specs e docs alinhados
- atualizar o menor conjunto correto de arquivos, mas não omitir fontes importantes da verdade

---

## Orientação de adapters

Use estes ativos do repositório corretamente:

- `.github/copilot-instructions.md` para comportamento global
- `.github/instructions/*.instructions.md` para comportamento com escopo por área
- `prompts/*.prompt.md` para fluxos de execução reutilizáveis
- `AGENTS.md` para separação de papéis e lógica de transição
- `CLAUDE.md` como ponto de entrada do adapter específico de Claude, não como fonte global de verdade do Copilot

---

## Nível de qualidade

Favoreça saída que seja:

- clara
- incremental
- revisável
- alinhada a padrões
- rastreável ao contexto do repositório

Evite saída que seja:

- genérica
- especulativa
- excessivamente abrangente
- desconectada da memória do repositório
- otimizada para velocidade em detrimento da manutenibilidade

---

## Postura padrão

Na dúvida:

- escolha o menor passo confiável
- preserve o comportamento
- torne as premissas visíveis
- mantenha a memória do projeto atualizada
- prefira progresso governado a velocidade ambígua
