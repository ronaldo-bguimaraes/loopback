# Plano — Ciclo 3

## Ações

### 1. Criar `.agents/agents/especulador.md`
- Agente tool-agnostic, markdown puro
- Dois modos de operação: `preflight` (define specs) e `audit` (valida)
- Critérios binários, evidências obrigatórias

### 2. Criar `.opencode/agents/especulador.md`
- Adaptador OpenCode com permissões read-only

### 3. Atualizar `opencode.json`
- Registrar especulador como subagent

### 4. Atualizar `.agents/agents/loopback.md`
- Adicionar especulador no ciclo:
  - Novo passo 0: especulador define specs → `docs/spec.md`
  - Passo 5: validador valida contra spec
  - Passo 7: especulador audit pós-ciclo

### 5. Atualizar `.opencode/agents/loopback.md`
- Adicionar task permission para especulador
