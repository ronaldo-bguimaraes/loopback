# Validação — Ciclo 3

## Agentes
- ✅ `.agents/agents/especulador.md` — criado com modo preflight + audit
- ✅ `.opencode/agents/especulador.md` — adaptador OpenCode
- ✅ `opencode.json` — especulador registrado como subagent

## Ciclo Loopback
- ✅ `.agents/agents/loopback.md` — passo 0 (especificação) + passo 7 (auditoria)
- ✅ Especulador nas dependências (`depends_on`)
- ✅ Spec first: ciclo não começa sem `docs/spec.md`
- ✅ Audit mandatory: ciclo não termina sem validação

## Consistência
- ✅ Especulador referenciado em `.agents/AGENTS.md`
- ✅ Especulador referenciado em `.opencode/agents/loopback.md` (task)
- ✅ 5 agentes no total: loopback, questionador, explicador, validador, especulador
- ✅ Zero frontmatter proprietário na fonte canônica
