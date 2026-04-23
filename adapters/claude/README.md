# Adapter Claude

Este adapter explica como o AEHF é entregue em ambientes estilo Claude.

O método AEHF permanece o mesmo.
O que muda é como o contexto de inicialização, a memória do repositório e as regras de execução são expostos à ferramenta.

---

## Propósito do adapter

O adapter Claude existe para:
- criar um contrato de inicialização curto e estrito
- reduzir ambiguidade no início da sessão
- forçar a ordem de leitura antes de trabalhos não triviais
- manter detalhes duráveis na memória do repositório em vez de sobrecarregar o ponto de entrada do adapter

---

## Ponto de entrada principal

Arquivo:
- `CLAUDE.md`

Este arquivo é o contrato de bootstrap de alta prioridade para ambientes estilo Claude.
Deve permanecer curto o suficiente para ser utilizável, mas forte o suficiente para fazer cumprir o método.

Seu papel é direcionar a ferramenta para as fontes reais de verdade, em vez de tentar manter todo o projeto em um único arquivo.

---

## Sequência de entrada obrigatória

Para trabalhos não triviais, comece com:

1. `README.md`
2. `docs/constitution/CONSTITUTION.md`
3. `docs/architecture/INVENTORY.md`
4. `docs/standards/TASK_DEPTH_POLICY.md`
5. `docs/standards/CODING_STANDARDS.md`
6. `docs/standards/DOC_UPDATE_POLICY.md`
7. `AGENTS.md`

Em seguida, consulte o contexto específico da tarefa conforme necessário:
- arquivos relevantes em `docs/domains/`
- pacote relevante em `specs/`
- decisões relacionadas em `docs/decisions/`
- lacunas ou discrepâncias em `docs/gaps/`

---

## Expectativas operacionais

Ao usar Claude com AEHF, o comportamento esperado é:

- classificar a profundidade da tarefa antes de decidir processo ou artefatos
- preservar o comportamento, a menos que a mudança intencional esteja documentada
- preferir mudança incremental em vez de reescrita
- usar a memória do repositório em vez de re-explicar o contexto em cada interação
- atualizar docs, specs e changelog quando ocorrer mudança significativa
- distinguir fatos de suposições
- escalar para validação humana quando o risco ou a ambiguidade for alta

---

## Por que este adapter é estruturado desta forma

Ambientes estilo Claude se beneficiam de um contrato de inicialização forte, mas também se beneficiam quando os detalhes duráveis permanecem fora do arquivo de bootstrap.

Este adapter, portanto, separa:
- um ponto de entrada conciso (`CLAUDE.md`)
- memória operacional durável (`docs/`)
- pacotes de mudança estruturados (`specs/`)
- fluxos de trabalho reutilizáveis (`prompts/`)

Essa separação mantém o método forte sem transformar o adapter em um despejo de contexto monolítico.

---

## Padrão de uso sugerido

Um fluxo de uso prático é:

1. começar pelo `CLAUDE.md`
2. seguir a ordem de leitura obrigatória
3. classificar a profundidade da tarefa
4. inspecionar os arquivos relevantes de domínio, spec, decisão e lacuna
5. executar incrementalmente
6. atualizar a memória do projeto como parte do mesmo pacote de mudança

---

## O que este adapter não é

Este adapter não é:
- um substituto completo para a documentação do repositório
- um arquivo gigante de memória do projeto
- um método separado do AEHF
- uma justificativa para ignorar specs ou padrões

É o mecanismo de bootstrap específico para Claude do mesmo modelo operacional universal AEHF.

---

## Regra final

Se qualquer atalho específico do Claude conflitar com a constituição ou os padrões do AEHF, o método central prevalece.
