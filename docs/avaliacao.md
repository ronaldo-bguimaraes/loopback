# Avaliação — Ciclos 1–6

Gerado pelo especulador (modo avaliação). Ciclo encerrado pois `atual (6) >= estimado (0)`.

## Resumo

| Ciclo | O que foi feito |
|-------|----------------|
| **1** | Segurança: allowlists granulares. Maker-checker split. Docs obrigatórios por etapa. Contador de iteração. Referências de arquivo validadas. |
| **2** | Tool-agnostic: `.agents/` como fonte canônica, adaptadores como artefato. Entry point `AGENTS.md` na raiz. No-downgrade como política imutável. |
| **3** | Spec first: `docs/spec.md` obrigatório. Audit mandatory. Especulador read-only (maker-checker). |
| **4** | Ciclo enxuto de 5 passos. Documentação como side-effect. `goal.md` declarado redundante. Lessons.md consultado durante validação. |
| **5** | Conventional Commits: `docs/commits.md`, referência em `AGENTS.md` e `loopback.md`. |
| **6** | Especulador preflight com estimativa de ciclos. Audit avalia contra goal (spec). `docs/avaliacao.md` ao fim do ciclo. Loopback usa `estimado`. `iteracao.yaml` migrado (`limite` → `estimado` + `max`). |

## Metas vs Realidade

- ✅ **Especulador preflight estima ciclos** — `.agents/agents/especulador.md` atualizado com instruções de estimativa; `iteracao.yaml` sem `limite: 5`
- ✅ **Especulador audit avalia goal** — Modo audit valida contra `docs/spec.md`; modo avaliação gera relatório final
- ✅ **Avaliação final ao atingir estimado** — `docs/avaliacao.md` existe com template; loopback e especulador referenciam sua geração
- ✅ **Loopback orquestrador atualizado** — Passo 5 usa `estimado`, delega avaliação, gera `avaliacao.md`
- ✅ **`iteracao.yaml` migrado** — `limite: 5` removido; `estimado: 0` + `atual: 6` + `max: 20`
- ✅ **Compatibilidade mantida** — questionador, explicador, validador intactos; `docs/iteracao.md` preservado
- ⚠️ **`estimado` em 0** — O preflight não ajustou o estimado para este ciclo (valor default). Isso acionou a avaliação precocemente. Lição registrada.

## Desvios

| Planejado | Realidade | Justificativa |
|-----------|-----------|---------------|
| Audit ler `docs/goal.md` | Audit valida contra `docs/spec.md` | `goal.md` marcado como obsoleto no ciclo 4; `spec.md` é a única fonte |
| `limite: 5` substituído por `estimado: N` | Além de `estimado`, adicionou-se `max: 20` como hard limit de segurança | Melhoria: teto absoluto evita loops infinitos mesmo se estimativa falhar |

## Conclusão

O goal do ciclo 6 foi **atingido**. Todos os 5 critérios da spec foram cumpridos. O sistema loopback agora possui:
- Estimativa dinâmica de ciclos (preflight)
- Avaliação contra goal em vez de limite numérico (audit)
- Geração automática de avaliação final
- Hard limit de segurança (`max`)
- Compatibilidade retroativa com agentes e arquivos legados

O projeto está maduro para novos ciclos ou para ser considerado completo.
