# Spec — Simplificação do Estado

## Critérios

- [x] **`ciclo-N/` → `memoria/`**: diretórios `ciclo-{1..7}/` removidos, `memoria/` criado com resumo histórico
- [x] **`.gitignore`**: `.agents/state/memoria/` ignorado (não `state/` inteiro)
- [x] **`especulador.md`**: 2 modos (spec + valida), sem estimativa, sem `ciclo-N/`
- [x] **`loopback.md`**: passo 5 = arquivar + loop guard, sem contadores
- [x] **Docs obsoletos removidos**: `avaliacao.md`, `iteracao.md`, `goal.md`, `aprendizados.md`
- [x] **`.agents/AGENTS.md`**: estrutura reflete `memoria/`, sem `ciclo-`, sem `estimado`
- [x] **`lessons.md` preservado**: existe com conteúdo, versionado
- [x] **Invariantes**: spec-first, audit mandatory, no-downgrade, maker-checker split
