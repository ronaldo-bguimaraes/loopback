# Loopback — Sistema Autoincremental Tool-Agnostic

Este projeto implementa um ciclo de desenvolvimento autoincremental para
agentes de IA, sem dependência de ferramenta específica.

## Estrutura

```
.agents/                    ← Fonte canônica (tool-agnostic)
  AGENTS.md                 ← Este arquivo — instruções do projeto
  agents/                   ← Definições de agente (markdown puro)
    loopback.md             ← Orquestrador do ciclo
    questionador.md         ← Crítico com pesquisa na internet
    explicador.md           ← Pesquisador e explicador técnico
    validador.md            ← Verificador independente
  policies/                 ← Políticas de segurança (imutáveis entre ciclos)
    security.yaml           ← Regras de segurança e no-downgrade
  state/                    ← Estado persistente entre ciclos
    iteracao.yaml           ← Contador de iterações
    lessons.md              ← Aprendizados acumulados
  skills/                   ← Skills portáveis
docs/                       ← Documentação do ciclo
  definicao.md
  hipoteses.md
  plano.md
  validacao.md
  melhoria.md
  goal.md
  aprendizados.md
  iteracao.md               ← Contador legado (manter compatibilidade)
AGENTS.md                   ← Entry point universal (raiz)
```

## Agentes

| Agente | Role | Descrição |
|---|---|---|
| loopback | orchestrator | Ciclo de 5 etapas: spec & definição → questionamento & plano → desenvolvimento → validação & melhoria → auditoria & loop |
| questionador | critic | Questiona com pesquisa na internet |
| explicador | researcher | Explica conceitos com pesquisa na internet |
| validador | checker | Executa testes e verifica critérios |
| especulador | specifier | Define specs antes do ciclo e valida após |

## Convenções

- Definições de agente em `.agents/agents/*.md` — markdown puro, sem frontmatter proprietário
- Memória entre ciclos em `.agents/state/`
- Documentação de ciclo em `docs/`
- Adaptadores tool-specific são gerados (`.opencode/`, `opencode.json`, etc.)
- **Commits seguem Conventional Commits** — veja `docs/commits.md`

## Regras

- **No-downgrade:** toda iteração deve melhorar o projeto em pelo menos um aspecto
- **Spec-first + estimativa:** especulador define critérios e estima ciclos no preflight
- **Audit mandatory:** especulador valida ao final de cada ciclo
- **Avaliação final:** quando `atual >= estimado`, gera `docs/avaliacao.md` e encerra
- **Hard limit:** `max` em `.agents/state/iteracao.yaml` para segurança

## Comandos

- Test: `npm test` / `pytest` / `cargo test`
- Lint: `npm run lint` / `ruff` / `golangci-lint`
- Typecheck: `npm run typecheck` / `mypy` / `cargo check`

## Gotchas (aprendidos)

- Não usar permissões irrestritas — preferir allowlists granulares
- Sempre criar agente validador separado (maker-checker split)
- Toda referência a arquivo deve existir antes de ser mencionada
- Sempre definir entry point universal (AGENTS.md na raiz)
