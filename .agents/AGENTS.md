# Loopback — Sistema Incremental Tool-Agnostic

Ciclo de desenvolvimento autoincremental para agentes de IA.

## Estrutura

```
.agents/                    ← Fonte canônica (tool-agnostic)
  AGENTS.md                 ← Este arquivo
  agents/                   ← Definições de agente (markdown puro)
    loopback.md             ← Orquestrador do ciclo (5 passos)
    questionador.md         ← Crítico com pesquisa na internet
    explicador.md           ← Pesquisador e explicador técnico
    validador.md            ← Verificador independente
    especulador.md          ← Spec e validação de critérios
  policies/                 ← Políticas de segurança (imutáveis)
    security.yaml
  state/                    ← Estado (transitório + persistente)
    memoria/                ← Memória de sessão (.gitignore)
    lessons.md              ← Aprendizados duradouros (versionado)
docs/                       ← Documentação do ciclo
AGENTS.md                   ← Entry point universal (raiz)
```

## Agentes

| Agente | Role | Descrição |
|---|---|---|
| loopback | orchestrator | Spec → Questionar → Desenvolver → Validar → Arquivar |
| questionador | critic | Desafia especificações com pesquisa na internet |
| explicador | researcher | Esclarece conceitos com pesquisa na internet |
| validador | checker | Executa verificações contra os critérios |
| especulador | specifier | Define critérios (spec) e valida resultados (audit) |

## Regras

- **No-downgrade:** toda iteração melhora o projeto em ao menos um aspecto
- **Spec-first + audit mandatory:** nenhum ciclo sem critérios e sem validação
- **Maker-checker split:** especulador ≠ implementador ≠ validador
- **Loop guard:** ciclos repetidos são detectados e alertados
- **Estado transitório:** `memoria/` é local e deletável; `lessons.md` é versionado
