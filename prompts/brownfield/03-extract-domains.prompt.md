# 03 - Extrair Domínios

## Propósito

Inferir limites de domínio a partir da implementação existente e do comportamento operacional.

## Quando usar

Após o inventário de componentes/dependências estar disponível.

## Entradas necessárias

- Inventário
- Fluxos de trabalho/casos de uso principais
- Conhecimento do time sobre propriedade

## Instruções para o AI

1. Agrupar módulos por capacidade de negócio.
2. Propor limites de domínio e interfaces.
3. Sinalizar riscos de acoplamento e sobreposição.
4. Sugerir docs de domínio candidatos a serem criados primeiro.

## Saídas esperadas

- Proposta de mapeamento de domínios
- Notas de risco de acoplamento
- Passos de documentação priorizados

## Critérios de conclusão

O modelo de domínio é suficientemente crível para suportar o fatiamento de modernização.
