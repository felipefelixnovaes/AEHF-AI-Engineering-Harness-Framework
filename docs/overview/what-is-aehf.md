# O que é o AEHF

AEHF (AI Engineering Harness Framework) é um framework universal para entrega de software assistida por AI de forma governada.

Foi projetado para equipes que desejam os benefícios de velocidade da AI sem aceitar a instabilidade, inconsistência e perda de contexto que frequentemente acompanham o uso ad hoc de AI.

O AEHF não é um provedor de modelos, não é uma IDE e não é uma camada de lock-in de plataforma.
É um **meta-framework** sobre como equipes de software estruturam a participação da AI na entrega.

---

## Em uma frase

O AEHF dá à AI um harness de engenharia estável: estrutura suficiente para ser confiável, flexibilidade suficiente para ser rápido.

---

## Qual problema ele resolve

Muitas equipes caem em uma de duas armadilhas:

### 1. vibe coding caótico
Os sintomas incluem:
- prompts sem estrutura durável
- memória fraca entre sessões
- mudanças inconsistentes entre colaboradores
- documentação ausente ou desatualizada
- muito retrabalho e manutenção frágil

### 2. Processo excessivamente pesado
Os sintomas incluem:
- artefatos demais para trabalhos pequenos
- burocracia que desacelera a entrega
- baixa adoção por equipes reais
- processo que parece rigoroso mas gera atrito

O AEHF existe para operar no meio útil:

**estrutura mínima estável + profundidade sob demanda**

---

## O que o AEHF oferece

O AEHF fornece um modelo operacional reutilizável para:

- alinhar a profundidade de planejamento ao risco da tarefa
- transformar documentação em memória operacional durável
- estruturar a execução em diferentes ferramentas de AI e colaboradores
- aplicar governança leve sem excesso ritual
- evoluir métodos e adapters sem quebrar a abordagem central

---

## O que o diferencia

O AEHF não compete com LLMs.
Ele coordena como LLMs participam da entrega de software.

Isso significa que pode funcionar junto com:
- Claude
- GitHub Copilot
- Cursor
- ferramentas baseadas em OpenAI
- ferramentas baseadas em Gemini
- ambientes com modelos locais
- adapters futuros ainda não definidos

O método permanece estável mesmo quando as ferramentas mudam.

---

## O que o AEHF não é

O AEHF não é:
- um framework de aplicação
- um artifício de geração de código
- um runtime multi-agente obrigatório
- uma suíte de processo empresarial pesada
- um substituto para o julgamento de engenharia

É um framework para tornar a engenharia assistida por AI mais governável, mais revisável e mais durável.

---

## Para quem é

O AEHF é especialmente útil para:
- desenvolvedores solo que querem velocidade sem caos
- startups que precisam de estrutura leve
- equipes modernizando sistemas legados
- fábricas de software que precisam de consistência entre repositórios
- equipes corporativas que precisam de auditabilidade e método sem sobrecarga de processo

---

## Resumo do modelo operacional

O AEHF funciona por meio de um modelo baseado no repositório:

- `docs/` guarda a memória operacional durável
- `specs/` guarda pacotes de mudança estruturados
- `prompts/` guarda workflows de execução reutilizáveis
- adapters controlam como diferentes ferramentas de AI consomem contexto
- padrões e governança mantêm a entrega proporcional e revisável

Isso torna o próprio repositório parte do sistema de entrega, não apenas um lugar para armazenar código e notas.
