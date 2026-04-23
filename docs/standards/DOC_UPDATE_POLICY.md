# Política de Atualização de Documentação

A documentação faz parte da entrega.
Não é trabalho posterior, decoração ou limpeza opcional.

No AEHF, a memória do repositório deve permanecer sincronizada com mudanças relevantes.
Esta política define quando a documentação deve ser atualizada, o que deve ser atualizado e como evitar deriva silenciosa.

---

## Regra fundamental

Quando comportamento, arquitetura, decisões, padrões ou entendimento operacional mudam, a documentação relevante deve ser atualizada no mesmo pacote de mudança.

Não faça merge de mudanças relevantes deixando conscientemente a memória central do repositório desatualizada.

---

## O que requer atualizações de documentação

Atualize a documentação relevante sempre que qualquer um dos itens a seguir mudar:

- comportamento visível para usuários, operadores ou integradores
- arquitetura ou limites de módulo
- regras ou premissas de domínio
- padrões, processos ou regras de governança
- procedimentos de release, validação ou operacionais
- lacunas conhecidas, discrepâncias ou riscos
- entendimento de arquitetura descoberto durante trabalho brownfield ou Reverse
- lições que devem influenciar execuções futuras

---

## Conjunto mínimo de sincronização

Para uma mudança relevante, revise e atualize o menor conjunto correto destes artefatos:

- arquivos afetados em `docs/`
- pacote de mudança afetado em `specs/`
- `CHANGELOG.md` para mudanças com impacto externo ou operacional
- ADRs para decisões de relevância arquitetural ou de política
- registros de lacuna ou discrepância quando novos problemas forem descobertos
- lições quando um aprendizado reutilizável for gerado

O objetivo não é atualizar tudo.
O objetivo é atualizar toda fonte de verdade que, de outra forma, se tornaria enganosa.

---

## Mapeamento típico de atualizações

### Se o comportamento observável mudar
Normalmente atualizar:
- pacote de spec relevante em `specs/`
- arquivos de domínio relevantes em `docs/domains/`
- docs de arquitetura relevantes se limites ou fluxos mudaram
- `CHANGELOG.md`

### Se o entendimento da arquitetura mudar
Normalmente atualizar:
- `docs/architecture/`
- docs de domínio relevantes
- ADRs se uma decisão foi tomada
- lacunas relevantes se trade-offs ou limitações permanecerem

### Se uma nova regra ou padrão for introduzido
Normalmente atualizar:
- `docs/standards/`
- `README.md` se as expectativas voltadas ao contribuidor mudaram
- `CONTRIBUTING.md` se o fluxo de contribuição mudou

### Se comportamento legado for descoberto durante trabalho Reverse
Normalmente atualizar:
- `docs/as-is/`
- `docs/gaps/`
- docs de domínio relevantes
- pacote de spec relacionado

### Se uma lição reutilizável emergir
Normalmente atualizar:
- `docs/lessons/`
- padrões relevantes se a lição se tornar uma regra durável

---

## Checklist de prevenção de deriva

Antes de concluir uma mudança, pergunte:

- A implementação ainda corresponde ao comportamento descrito?
- Os docs ainda descrevem as premissas e restrições atuais?
- O entendimento da arquitetura mudou?
- Foi tomada uma decisão que merece um ADR?
- Foi descoberta uma lacuna, discrepância ou risco operacional?
- O changelog está atualizado para a mudança relevante?
- Um novo contribuidor seria enganado se os docs fossem deixados como estão?

Se a resposta a qualquer uma dessas perguntas for sim, atualize a memória relevante do repositório.

---

## Anti-padrões

Evite:

- adiar atualizações óbvias de docs para uma limpeza vaga no futuro
- tratar docs desatualizados como aceitáveis porque o código é "a verdadeira fonte de verdade"
- mudar comportamento sob o rótulo de refatoração sem atualizar a memória
- atualizar em excesso documentos não relacionados apenas para parecer minucioso
- escrever docs aspiracionais que não refletem a realidade atual

---

## Barra de qualidade

Boas atualizações de documentação são:

- factuais
- direcionadas
- duráveis
- alinhadas com a implementação e decisões reais
- úteis para futuros contribuidores e ferramentas de AI

Más atualizações de documentação são:

- vagas
- excessivamente amplas
- desconectadas da realidade
- omitem a fonte de verdade real que mudou

---

## Regra final

Se uma mudança relevante fizer com que futuros leitores, contribuidores ou ferramentas de AI formem um entendimento incorreto do sistema, a atualização da documentação não é opcional.
