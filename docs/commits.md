# Convenções de Commit

Este projeto segue **Conventional Commits** (conventionalcommits.org).

## Formato

```
<tipo>(<escopo>): <descrição>

<corpo (opcional, explica o porquê)>

<rodapé (opcional)>
```

## Tipos

| Tipo | Quando usar |
|---|---|
| `feat` | Nova funcionalidade |
| `fix` | Correção de bug |
| `docs` | Documentação apenas |
| `refactor` | Mudança estrutural sem mudar comportamento |
| `perf` | Melhoria de performance |
| `test` | Adição ou correção de testes |
| `chore` | Manutenção (deps, config, build) |
| `ci` | Configuração de CI/CD |
| `style` | Formatação, lint (sem mudar lógica) |

## Escopos

| Escopo | Área |
|---|---|
| `cycle` | Ciclo loopback e seus passos |
| `agents` | Definições de agente |
| `adapter` | Adaptadores tool-specific |
| `docs` | Documentação do projeto |
| `spec` | Especificação de ciclo |
| `policy` | Políticas de segurança |

## Regras

1. **Título ≤ 50 caracteres** — sem ponto final
2. **Modo imperativo**: "Add feature" (não "Added" ou "Adding")
3. **Corpo explica o *why*** — o *what* já está no diff
4. **Commits atômicos** — uma mudança lógica por commit
5. **Linhas do corpo ≤ 72 caracteres**
6. **Breaking changes**: use `!` após o tipo/escopo: `refactor(api)!: remove legacy endpoint`

## Exemplos

```
feat(agents): add especulador preflight mode

Spec-first requires criteria to be defined before implementation.
The especulador now validates that every cycle has binary, falsifiable
criteria before allowing execution to proceed.
```

```
refactor(cycle): simplify from 8 to 5 steps

Dedicated docs step created overhead without adding traceability.
Merging it into questionamento makes docs a continuous side-effect.
```

```
docs(commits): add commit conventions
```
