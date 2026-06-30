# Spec — Ciclo 4 — Simplificação do Ciclo

## Critérios
- [x] **Ciclo reduzido a 5 passos contínuos**: loopback.md define exatas 5 etapas
  - Evidência: 5 ocorrências de "### Passo" no arquivo
  - Status: ✅
- [x] **`docs/goal.md` eliminado**: spec.md é única fonte da verdade
  - Evidência: goal.md contém redirecionamento para spec.md
  - Status: ✅
- [x] **Lessons.md consultado na validação**: referenciado no passo de validação
  - Evidência: `grep "lessons.md" .agents/agents/loopback.md` mostra múltiplas referências, inclusive no passo 4
  - Status: ✅
- [x] **Nenhum passo exclusivo de documentação**: docs é contínuo, não etapa separada
  - Evidência: única menção é "Documentação é contínua" (preamble)
  - Status: ✅
- [x] **No-regression**: todos os elementos críticos preservados
  - Evidência: Preflight ✅ Audit ✅ Spec first ✅ Audit mandatory ✅ Validador ✅
  - Status: ✅
