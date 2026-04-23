# AI Engineering Harness Framework (AEHF)

**Pare o vibe coding. Comece a engenharia de AI governada.**

AEHF é um framework open-source para entrega de software assistida por AI.
Ele ajuda equipes a se moverem mais rápido sem perder estrutura, e a adicionar controle sem criar processos pesados.

O AEHF foi construído para o espaço entre dois extremos problemáticos:

- **vibe coding caótico** — saída rápida, memória fraca, qualidade inconsistente, alto retrabalho
- **burocracia de processo pesado** — rituais rígidos, entrega lenta, baixa adoção, esforço desperdiçado

Seu princípio operacional central é:

> **Estrutura estável mínima + profundidade sob demanda**

---

## Ideia central

**O AEHF fornece ao AI um harness de engenharia estável: estrutura suficiente para permanecer confiável, flexibilidade suficiente para permanecer rápido.**

---

## Por que o AEHF existe

AI pode gerar código rapidamente, mas velocidade sozinha não cria entrega de software confiável.

Em projetos reais, equipes enfrentam os mesmos problemas repetidamente:

- o contexto se perde entre sessões e contribuidores
- a implementação se afasta da documentação
- sistemas legados permanecem mal compreendidos
- a profundidade da mudança não corresponde à profundidade do processo
- cada ferramenta inventa seu próprio fluxo de trabalho
- prompts se tornam dívida operacional

O AEHF fornece um modelo operacional universal para engenharia de software assistida por AI por meio de:

- specs adaptativas
- memória de projeto durável
- controle de execução
- governança leve
- evolução contínua

É intencionalmente **agnóstico de plataforma** e não está vinculado a nenhum sistema interno.

---

## O que o AEHF é

- um framework para entrega de software assistida por AI governada
- um modelo operacional de repositório para engenharia de AI
- uma estrutura durável de documentação e memória
- um método amigável a adapters de ferramentas que funciona em diferentes ecossistemas

## O que o AEHF não é

- um substituto para LLMs
- um runtime multi-agente por padrão
- um conjunto de processos empresariais pesados
- um gerador de aplicações disfarçado de framework

---

## Os 5 pilares

1. **Specs Adaptativas**  
   Use o nível certo de rigor para a tarefa: Fast, Standard, Deep ou Reverse.
2. **Memória de Projeto**  
   Mantenha arquitetura, decisões, domínios, lacunas e lições como memória operacional durável.
3. **Execution Harness**  
   Oriente qual modelo, fluxo de trabalho e caminho de validação usar com base em risco e custo.
4. **Governança Leve**  
   Mantenha o controle por meio de ADRs, changelogs, verificações de lançamento e política de documentação.
5. **Evolução Embutida**  
   Expanda com segurança para novas ferramentas, adapters e modelos operacionais sem quebrar o método central.

---

## Por que o AEHF melhora a engenharia de AI

O AEHF melhora a entrega de AI no mundo real ao reduzir:

- prompts ambíguos
- despejo repetido de contexto
- premissas não documentadas
- desvio de fluxo de trabalho entre contribuidores
- divergência silenciosa entre código e docs

E melhora:

- consistência
- revisabilidade
- onboarding
- manutenibilidade
- eficiência de custo

---

## Para quem é este framework

- desenvolvedores solo
- startups
- fábricas de software
- equipes de entrega empresarial
- equipes modernizando sistemas legados

---

## Estrutura do repositório

```text
README.md                    # guia de início e ponto de entrada do framework
CLAUDE.md                    # ponto de entrada estrito do adapter para agentes no estilo Claude
AGENTS.md                    # papéis operacionais de agentes e limites
CHANGELOG.md                 # log de evolução do framework
CONTRIBUTING.md              # fluxo de contribuição e nível de qualidade

docs/                        # memória operacional durável (fonte da verdade)
specs/                       # pacote de execução por mudança e templates
prompts/                     # biblioteca operacional de prompts reutilizáveis
adapters/                    # orientação de entrega de contexto específica por ferramenta
examples/                    # pontos de partida de adoção orientados a cenários
.github/                     # instruções do copilot, templates de issue/PR
```

---

## Obtenha valor em 15 minutos

- Use `prompts/greenfield/` para iniciar um novo projeto com estrutura.
- Use `prompts/brownfield/` para mapear e estabilizar um repositório legado.
- Use `docs/standards/TASK_DEPTH_POLICY.md` para classificar o trabalho.
- Use `specs/templates/` para empacotar mudanças com segurança.
- Use adapters para entregar contexto à sua ferramenta de AI preferida.

---

## Início rápido

1. Clone este repositório como sua base de framework.
2. Leia `docs/constitution/CONSTITUTION.md`.
3. Escolha seu caminho inicial:
   - **greenfield**: comece em `prompts/greenfield/`
   - **brownfield**: comece em `prompts/brownfield/`
4. Classifique a profundidade da tarefa usando `docs/standards/TASK_DEPTH_POLICY.md`.
5. Crie specs em `specs/` a partir dos templates correspondentes.
6. Execute as mudanças e mantenha `docs/` atualizado conforme `docs/standards/DOC_UPDATE_POLICY.md`.

---

## Fluxo de trabalho greenfield (sugerido)

1. Inicialize a intenção e restrições do projeto (`01-bootstrap-project`).
2. Rascunhe a arquitetura inicial (`02-first-architecture`).
3. Crie o mapa de domínios (`03-create-domain-map`).
4. Construa a spec de funcionalidade (`04-create-feature-spec`).
5. Implemente iterativamente com verificações de governança (`05-implement-feature`).

Artefatos para priorizar:

- `specs/templates/standard-spec.template.md`
- `docs/architecture/REPOSITORY_MODEL.md`
- `docs/domains/DOMAIN_TEMPLATE.md`
- `docs/decisions/ADR_TEMPLATE.md`

---

## Fluxo de trabalho brownfield (sugerido)

1. Analise o repositório existente e as restrições (`01-analyze-repo`).
2. Construa o inventário do estado atual (`02-create-inventory`).
3. Extraia domínios implícitos (`03-extract-domains`).
4. Detecte pontos críticos e risco operacional (`04-detect-hotspots`).
5. Revele padrões implícitos (`05-map-implicit-standards`).

Para planejamento de modernização, continue com `prompts/reverse/`.

---

## Modelo de adapters

O método AEHF é universal; **a entrega de contexto é específica por adapter**.

- **Adapter Claude**: `CLAUDE.md` é o ponto de entrada estrito de memória.
- **Adapter Copilot**:
  - regras globais em `.github/copilot-instructions.md`
  - regras com escopo em `.github/instructions/*.instructions.md`
  - operações de prompt reutilizáveis em `prompts/*.prompt.md`
- **Adapter genérico**: documentado em `adapters/generic/README.md`.

---

## Roadmap

### v0.2

- variantes mais ricas de prompts para cenários de teste e migração
- playbooks de exemplo adicionais para ambientes regulados
- links cruzados mais fortes entre docs/specs/prompts

### v1.0

- expansão de adapters para ecossistemas adicionais de ferramentas de AI
- scaffolding opcional de CLI sem acoplamento ao método central
- padrões opcionais de telemetria/dashboard para insights de governança

---

## Contribuindo

Veja `CONTRIBUTING.md` para o fluxo de contribuição, padrões de qualidade e expectativas de revisão.

Se você mudar o comportamento, atualize docs/specs/changelog no mesmo pacote de mudança.

---

## Licença

MIT — veja `LICENSE`.
