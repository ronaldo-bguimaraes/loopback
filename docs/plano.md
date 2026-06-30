# Plano — Simplificação do Estado

## Ordem de implementação

1. **Criar `memoria/`** — resumo do histórico em `.md` narrativo
2. **Remover `ciclo-{1..7}/`** — após copiar resumo
3. **`.gitignore`** — adicionar `.agents/state/memoria/` (e só memoria, não state inteiro)
4. **Reescrever `especulador.md`** — 2 modos, sem estimativa/snapshot/avaliação
5. **Reescrever `loopback.md`** — passo 5 = arquivar + loop guard
6. **Limpar `docs/`** — remover `avaliacao.md`, `iteracao.md`
7. **Atualizar `.agents/AGENTS.md`** — estrutura reflete `memoria/`
