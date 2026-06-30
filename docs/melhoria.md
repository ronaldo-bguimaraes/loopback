# Melhoria — Ciclo 3

## Novos Agentes
- **especulador** — agente de especificação e auditoria de ciclo
  - Modo preflight: define specs antes do ciclo começar
  - Modo audit: valida se specs foram cumpridas ao final

## Ciclo Loopback
- Novo passo 0 (Especificação): especulador escreve `docs/spec.md`
- Passo 5 atualizado: validador valida contra a spec
- Passo 7 atualizado: especulador audita specs no loop

## Regras
- Spec first: nenhum ciclo começa sem critérios verificáveis
- Audit mandatory: nenhum ciclo termina sem validação
