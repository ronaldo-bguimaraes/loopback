# Loopback

Sistema autoincremental tool-agnostic para agentes de IA.

Um ciclo de desenvolvimento que se auto-alimenta: definir specs, questionar,
documentar, implementar, validar, melhorar e repetir — sem dependência de
ferramenta específica (OpenCode, Claude Code, Cursor, Windsurf, etc.).

## Estrutura

```
.agents/              ← Fonte canônica (tool-agnostic)
├── agents/           ← 5 agentes em markdown puro
├── policies/         ← Segurança + no-downgrade
└── state/            ← Memória entre ciclos
AGENTS.md             ← Entry point universal (30+ ferramentas)
docs/                 ← Documentação do ciclo
```

## Agentes

| Agente | Role | Descrição |
|---|---|---|
| **loopback** | orchestrator | Ciclo de 7 etapas: especificar → definir → questionar → documentar → desenvolver → validar → melhorar → auditar |
| **questionador** | critic | Questiona decisões com pesquisa na internet |
| **explicador** | researcher | Explica conceitos com pesquisa na internet |
| **validador** | checker | Executa testes e verifica critérios |
| **especulador** | specifier | Define specs antes do ciclo e valida após |

## Ciclo

```
1. Spec & Definição     → especulador define critérios, propósito
2. Questionamento & Plano → pesquisa, hipóteses, plano
3. Desenvolvimento       → implementação alinhada à spec
4. Validação & Melhoria  → testes contra spec + refatoração
5. Auditoria & Loop      → especulador audita, itera ou para
```

## Regras

- **No-downgrade:** toda iteração deve melhorar o projeto em ao menos um aspecto
- **Spec first:** nenhum ciclo começa sem critérios verificáveis
- **Audit mandatory:** nenhum ciclo termina sem validação
- **Maker-checker split:** quem especifica ≠ quem implementa ≠ quem valida

## Como usar

1. Clone o repositório
2. Abra com sua ferramenta de IA favorita (lê `AGENTS.md` automaticamente)
3. Ative o agente **loopback** e descreva o que quer desenvolver
4. O ciclo roda sozinho: especula, questiona, documenta, implementa, valida, melhora

### Adaptadores

Se você usa **OpenCode**, o adaptador já está em `.opencode/` e `opencode.json`.
Para outras ferramentas, gere o adaptador correspondente a partir de `.agents/`.

---

**Criado pelo próprio loopback** — cada ciclo melhora o projeto que o define.
