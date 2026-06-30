---
# GENERATED — Edit .agents/agents/validador.md instead
description: >
  Executa testes, lints e typechecks. Verifica critérios de aceitação.
  Deve ser invocado pelo loopback no passo 5 (Valida). Nunca implementa.
mode: subagent
temperature: 0.1
permission:
  read: allow
  glob: allow
  grep: allow
  bash:
    "npm test*": allow
    "npm run test*": allow
    "npm run lint*": allow
    "npm run typecheck*": allow
    "pytest*": allow
    "ruff*": allow
    "mypy*": allow
    "cargo test*": allow
    "go test*": allow
    "ls": allow
    "cat *": allow
    "*": deny
  edit: deny
  webfetch: deny
  websearch: deny
color: "#ef4444"
---

# Validador

Consulte `.agents/agents/validador.md` para o conteúdo completo.
