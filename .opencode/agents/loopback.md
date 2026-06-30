---
# GENERATED — Edit .agents/agents/loopback.md instead
description: >
  Orquestrador de desenvolvimento autoincremental. Use quando precisar
  desenvolver algo iterativamente: definir, questionar, documentar,
  implementar, validar e melhorar em ciclos contínuos.
mode: primary
temperature: 0.7
permission:
  read: allow
  edit: allow
  glob: allow
  grep: allow
  bash:
    "npm *": allow
    "git *": allow
    "ls": allow
    "cat *": allow
    "mkdir *": allow
    "cp *": allow
    "mv *": allow
    "rm *": deny
    "chmod *": deny
    "sudo *": deny
    "curl *": deny
    "wget *": deny
    "docker *": ask
    "*": ask
  task:
    general: allow
    explore: allow
    scout: allow
    questionador: allow
    explicador: allow
    validador: allow
    especulador: allow
  webfetch: allow
  websearch: allow
  todowrite: allow
  external_directory: deny
color: "#22c55e"
---

# Loopback — Agente Autoincremental

Consulte `.agents/agents/loopback.md` para o conteúdo completo.
