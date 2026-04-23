# AI Engineering Harness Framework (AEHF)

> 🇺🇸 Read in English: [README.md](README.md)

**Pare de fazer vibe coding. Comece a engenharia de software com IA governada.**

AEHF é um framework open source para entrega de software assistida por IA.
Ele ajuda equipes a avançar mais rápido sem perder estrutura e a adicionar controle sem criar processos pesados.

O AEHF foi criado para o espaço entre dois extremos quebrados:

- **vibe coding caótico** — saída rápida, memória fraca, qualidade inconsistente, alto retrabalho
- **burocracia de processo pesada** — rituais rígidos, entrega lenta, baixa adoção, desperdício de esforço

Seu princípio operacional central é:

> **Estrutura mínima estável + profundidade sob demanda**

---

## Ideia central

**O AEHF dá à IA um harness de engenharia estável: estrutura suficiente para manter confiabilidade e flexibilidade suficiente para manter velocidade.**

---

## Por que o AEHF existe

A IA pode gerar código rapidamente, mas velocidade sozinha não cria uma entrega de software confiável.

Em projetos reais, as equipes enfrentam repetidamente os mesmos problemas:

- contexto se perde entre sessões e contribuidores
- implementação se afasta da documentação
- sistemas legados continuam pouco compreendidos
- profundidade da mudança não é combinada com profundidade do processo
- cada ferramenta inventa seu próprio fluxo
- prompts viram dívida operacional

O AEHF fornece um modelo operacional universal para engenharia de software assistida por IA por meio de:

- specs adaptativas
- memória durável de projeto
- controle de execução
- governança leve
- evolução contínua

Ele é intencionalmente **agnóstico de plataforma** e não depende do Mission Control nem de qualquer sistema interno.

---

## O que é o AEHF

- um framework para entrega de software assistida por IA com governança
- um modelo de operação de repositório para engenharia com IA
- uma estrutura de documentação e memória durável
- um método compatível com adaptadores para diferentes ecossistemas de ferramentas

## O que o AEHF não é

- um substituto para LLMs
- um runtime multiagente por padrão
- uma suíte de processos corporativos pesada
- um gerador de aplicações disfarçado de framework

---

## Os 5 pilares

1. **Specs adaptativas**  
   Use o nível de rigor certo para a tarefa: Fast, Standard, Deep ou Reverse.
2. **Memória de projeto**  
   Mantenha arquitetura, decisões, domínios, gaps e lições como memória operacional durável.
3. **Harness de execução**  
   Oriente qual modelo, fluxo e caminho de validação usar com base em risco e custo.
4. **Governança leve**  
   Mantenha controle com ADRs, changelogs, checklists de release e política de documentação.
5. **Evolução embutida**  
   Expanda com segurança para novas ferramentas, adaptadores e modelos operacionais sem quebrar o método central.

---

## Por que o AEHF melhora a engenharia com IA

O AEHF melhora a entrega real com IA reduzindo:

- prompts ambíguos
- despejo repetido de contexto
- premissas não documentadas
- desvio de fluxo entre contribuidores
- divergência silenciosa entre código e docs

E melhora:

- consistência
- revisabilidade
- onboarding
- manutenibilidade
- eficiência de custo

---

## Para quem é

- desenvolvedores solo
- startups
- fábricas de software
- equipes corporativas de entrega
- equipes modernizando sistemas legados

---

## Estrutura do repositório

```text
README.md                    # guia de entrada e ponto inicial do framework
CLAUDE.md                    # ponto de entrada estrito para agentes estilo Claude
AGENTS.md                    # papéis operacionais e limites
CHANGELOG.md                 # histórico de evolução do framework
CONTRIBUTING.md              # fluxo de contribuição e nível de qualidade

docs/                        # memória operacional durável (fonte da verdade)
specs/                       # pacote de execução por mudança
prompts/                     # biblioteca reutilizável de prompts operacionais
adapters/                    # orientação de contexto específica por ferramenta
examples/                    # pontos de partida orientados a cenários
.github/                     # instruções do Copilot e templates de issue/PR
```

---

## Gere valor em 15 minutos

- Use `prompts/greenfield/` para iniciar um novo projeto com estrutura.
- Use `prompts/brownfield/` para mapear e estabilizar um repositório legado.
- Use `docs/standards/TASK_DEPTH_POLICY.md` para classificar o trabalho.
- Use `specs/templates/` para empacotar mudanças com segurança.
- Use adaptadores para entregar contexto à ferramenta de IA da sua escolha.

---

## Início rápido

1. Clone este repositório como base do framework.
2. Leia `docs/constitution/CONSTITUTION.md`.
3. Escolha seu caminho inicial:
   - **greenfield**: comece por `prompts/greenfield/`
   - **brownfield**: comece por `prompts/brownfield/`
4. Classifique a profundidade da tarefa usando `docs/standards/TASK_DEPTH_POLICY.md`.
5. Crie specs em `specs/` a partir dos templates correspondentes.
6. Execute as mudanças e mantenha `docs/` atualizada segundo `docs/standards/DOC_UPDATE_POLICY.md`.

---

## Fluxo Greenfield (sugerido)

1. Inicialize intenção e restrições do projeto (`01-bootstrap-project`).
2. Rascunhe a arquitetura inicial (`02-first-architecture`).
3. Crie o mapa de domínios (`03-create-domain-map`).
4. Construa a spec da funcionalidade (`04-create-feature-spec`).
5. Implemente de forma iterativa com checagens de governança (`05-implement-feature`).

Artefatos para priorizar:

- `specs/templates/standard-spec.template.md`
- `docs/architecture/REPOSITORY_MODEL.md`
- `docs/domains/DOMAIN_TEMPLATE.md`
- `docs/decisions/ADR_TEMPLATE.md`

---

## Fluxo Brownfield (sugerido)

1. Analise o repositório existente e as restrições (`01-analyze-repo`).
2. Monte o inventário do estado atual (`02-create-inventory`).
3. Extraia domínios implícitos (`03-extract-domains`).
4. Detecte hotspots e risco operacional (`04-detect-hotspots`).
5. Traga à tona padrões implícitos (`05-map-implicit-standards`).

Para planejamento de modernização, continue com `prompts/reverse/`.

---

## Modelo de adaptadores

O método AEHF é universal; a **entrega de contexto é específica por adaptador**.

- **Adaptador Claude**: `CLAUDE.md` é o ponto de entrada estrito de memória.
- **Adaptador Copilot**:
  - regras globais em `.github/copilot-instructions.md`
  - regras por escopo em `.github/instructions/*.instructions.md`
  - operações reutilizáveis de prompt em `prompts/*.prompt.md`
- **Adaptador genérico**: documentado em `adapters/generic/README.md`.

---

## Roadmap

### v0.2

- variantes de prompt mais ricas para cenários de teste e migração
- playbooks de exemplo adicionais para ambientes regulados
- links cruzados mais fortes entre docs/specs/prompts

### v1.0

- expansão de adaptadores para ecossistemas adicionais de ferramentas de IA
- scaffolding opcional via CLI sem acoplar o método central
- padrões opcionais de telemetria/dashboard para insights de governança

---

## Contribuindo

Veja `CONTRIBUTING.md` para fluxo de contribuição, padrões de qualidade e expectativas de revisão.

Se você mudar comportamento, atualize docs/specs/changelog no mesmo pacote de mudança.

---

## Licença

MIT — veja `LICENSE`.
