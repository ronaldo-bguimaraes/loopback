# Hipóteses — Ciclo 3

### Hipótese 1: Um agente pode fazer os dois papéis (definir + validar)
- Risco de viés de confirmação (mesmo agente não falha a própria spec)
- Mitigação: specs com critérios binários + evidências obrigatórias
- O validador (separado) executa os testes contra a spec

### Hipótese 2: Spec em markdown puro é suficiente
- Formato checklist tool-agnostic, sem schema proprietário
- Qualquer LLM lê e verifica

### Hipótese 3: Especulador deve ser invocado automaticamente
- Passo 0 (preflight) + Passo 7 (audit) dentro do ciclo loopback
- Sem intervenção humana
