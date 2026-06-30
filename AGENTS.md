# Loopback

Sistema autoincremental tool-agnostic para agentes de IA.

**Fonte da verdade:** `.agents/AGENTS.md` — leia lá para documentação completa.

## Resumo

- **Orquestrador**: `.agents/agents/loopback.md` — ciclo de 7 etapas
- **Subagentes**: `.agents/agents/questionador.md`, `explicador.md`, `validador.md`
- **Memória**: `.agents/state/lessons.md`
- **Políticas**: `.agents/policies/security.yaml`
- **Docs do ciclo**: `docs/`

## Adaptadores Tool-Specific

| Tool | Localização | Status |
|---|---|---|
| OpenCode | `.opencode/agents/*.md` + `opencode.json` | Gerado de `.agents/` |
| Claude Code | `CLAUDE.md` | Symlink |
| Cursor | `.cursor/rules/` | Gerado |

## Regra

**No-downgrade:** toda iteração deve melhorar o projeto em ao menos um aspecto.
