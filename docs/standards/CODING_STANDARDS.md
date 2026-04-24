# Padrões de Código

Estes padrões são intencionalmente concisos e universais.

## Regras fundamentais

- Preserve o comportamento existente, a menos que uma mudança seja intencional e documentada.
- Prefira mudanças incrementais a reescritas amplas.
- Mantenha as mudanças delimitadas e reversíveis.
- Torne as premissas explícitas em specs/revisões.
- Mantenha testes e validação alinhados ao nível de risco.

## Mudanças sensíveis a código legado

- Use touch-and-raise: melhore apenas a área tocada + melhorias imediatas de segurança.
- Evite substituição especulativa de arquitetura.
- Documente restrições descobertas e contratos implícitos.

## Regras de contribuição assistida por AI

- Não invente APIs ou comportamentos sem evidências.
- Verifique as mudanças geradas em relação às convenções do repositório.
- Atualize os docs quando comportamento, interfaces ou fluxo operacional mudar.
