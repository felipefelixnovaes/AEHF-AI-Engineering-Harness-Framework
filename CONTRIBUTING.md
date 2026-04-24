# Contribuindo com o AEHF

Obrigado por contribuir com o AEHF.

Este repositório não é apenas uma coleção de templates e prompts.
É um repositório de framework, portanto a qualidade da contribuição depende de clareza, consistência e respeito ao método.

As contribuições devem tornar o framework:
- mais útil
- mais coerente
- mais portátil
- mais confiável
- mais fácil de adotar em repositórios reais

---

## Princípios de contribuição

Todas as contribuições devem seguir estes princípios:

- manter as mudanças incrementais e revisáveis
- preservar o comportamento existente salvo se a mudança for intencional e documentada
- alinhar cada mudança com a constituição e os padrões do AEHF
- preferir clareza a novidade
- preferir melhorias duráveis a gambiarras locais inteligentes
- tratar a documentação como parte da entrega, não como reflexão tardia

Antes de contribuir, leia:
- `README.md`
- `docs/constitution/CONSTITUTION.md`
- `docs/standards/TASK_DEPTH_POLICY.md`
- `docs/standards/DOC_UPDATE_POLICY.md`

---

## Quais tipos de contribuições são bem-vindas

Exemplos de contribuições valiosas:

- templates mais robustos
- padrões mais claros
- melhores arquivos de prompt
- orientação aprimorada de adapters
- exemplos adicionais
- orientação de repositório multiplataforma
- melhorias de governança que permaneçam leves
- correções de ambiguidade, inconsistência ou desvio no próprio framework

Contribuições menos valiosas incluem:
- verbosidade desnecessária
- dependência de ferramenta específica sem bom motivo
- expansão especulativa sem valor claro de adoção
- mudanças cosméticas que reduzem clareza ou aumentam ruído

---

## Fluxo de trabalho básico

1. Alinhe sobre o problema ou escopo.
2. Classifique a profundidade da tarefa usando `docs/standards/TASK_DEPTH_POLICY.md`.
3. Crie ou atualize o pacote de mudança apropriado em `specs/templates/` quando necessário.
4. Implemente em fatias pequenas e revisáveis.
5. Atualize a documentação conforme `docs/standards/DOC_UPDATE_POLICY.md`.
6. Adicione um ADR quando a decisão for significativa para arquitetura ou processo.
7. Atualize `CHANGELOG.md` para mudanças notáveis no framework.
8. Envie um PR usando `.github/pull_request_template.md`.

---

## Orientação de contribuição por tipo de mudança

### Mudanças de documentação e padrões
Devem:
- melhorar a clareza
- reduzir ambiguidades
- permanecer consistentes com o método AEHF
- evitar introduzir contradições entre arquivos

### Mudanças na biblioteca de prompts
Devem:
- ser reutilizáveis
- ser orientadas a resultados
- definir claramente propósito, entradas, saídas esperadas e critérios de conclusão
- evitar teatro de prompt superficial

### Mudanças de adapters
Devem:
- preservar o método universal do AEHF
- melhorar a entrega de contexto para um ecossistema específico
- evitar alterar princípios centrais apenas porque uma ferramenta se comporta de forma diferente

### Mudanças de exemplos
Devem:
- reduzir abstração
- mostrar caminhos práticos de adoção
- permanecer realistas e orientados a cenários

---

## Expectativas de qualidade

Não envie contribuições que:
- dependam de reescritas especulativas
- introduzam mudanças de comportamento não documentadas
- deixem a memória do repositório desatualizada
- adicionem complexidade sem melhorar adoção ou clareza
- fragmentem o framework em versões incompatíveis específicas de ferramentas

Contribuições fortes geralmente:
- melhoram a usabilidade sem inflar o framework
- tornam a memória do repositório mais durável
- fortalecem a relação entre docs, specs, prompts e adapters
- ajudam futuros contribuidores a tomar melhores decisões mais rapidamente

---

## Critérios de aceitação de PR

Um PR tem maior probabilidade de ser aceito quando:

- o escopo é claro e delimitado
- a profundidade de tarefa selecionada é apropriada
- os artefatos necessários para essa profundidade estão presentes
- docs, specs e memória do repositório estão sincronizados
- riscos e premissas são explícitos
- a mudança melhora clareza, utilidade ou confiabilidade
- o framework permanece portátil e consistente com o método

---

## Mentalidade de revisão

A revisão neste repositório não é apenas sobre se o texto ou a estrutura parece bom.
É sobre se a contribuição fortalece o framework como método operacional.

Os revisores podem rejeitar mudanças que são tecnicamente corretas, mas que:
- incham o framework
- enfraquecem a portabilidade
- criam contradição entre artefatos
- otimizam para novidade em vez de utilidade durável

---

## Regra final

Contribua de forma que torne o AEHF mais fácil de confiar, mais fácil de adotar e mais fácil de evoluir.

Se uma mudança torna o repositório mais barulhento mas não mais claro, provavelmente não é uma boa contribuição.
