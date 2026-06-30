# Spec — Ciclo 6

## Critérios

- [ ] **Especulador preflight estima ciclos**: `.agents/agents/especulador.md` deve ser atualizado para que, no modo preflight, o especulador leia o estado do projeto, estime quantos ciclos são necessários para atingir o goal, e registre o estimado em `.agents/state/iteracao.yaml` no formato `estimado: N` (substituindo `limite: 5`)
  - Evidência: `.agents/agents/especulador.md` contém instrução de estimativa + `.agents/state/iteracao.yaml` não contém mais `limite: 5`
  - Status:

- [ ] **Especulador audit avalia goal, não limite numérico**: `.agents/agents/especulador.md` deve ser atualizado para que, no modo audit, o especulador avalie se o **goal foi atingido** (lendo `docs/goal.md` e validando evidências), e não apenas se o limite numérico de ciclos foi atingido
  - Evidência: `.agents/agents/especulador.md` contém instrução de avaliação contra goal
  - Status:

- [ ] **Avaliação final ao atingir estimado**: Quando `atual >= estimado` em `iteracao.yaml`, o especulador (ou o loopback) deve gerar `docs/avaliacao.md` com: (a) o que foi feito no ciclo, (b) o que fugiu do planejado, (c) se o goal foi atingido
  - Evidência: arquivo `docs/avaliacao.md` existe e contém template/estrutura; `.agents/agents/loopback.md` ou `.agents/agents/especulador.md` referencia sua geração
  - Status:

- [ ] **Loopback orquestrador atualizado**: `.agents/agents/loopback.md` passo 5 (auditoria) deve: (a) usar `estimado` em vez de `limite`, (b) delegar ao especulador a avaliação de goal, (c) gerar `docs/avaliacao.md` quando `atual >= estimado`
  - Evidência: `.agents/agents/loopback.md` não referencia mais limite fixo; contém lógica de avaliação contra goal e geração de `docs/avaliacao.md`
  - Status:

- [ ] **`iteracao.yaml` migrado**: `.agents/state/iteracao.yaml` muda de `limite: 5` / `atual: N` para `estimado: N` / `atual: N`; o especulador preflight define `estimado`; `limite: 5` é removido
  - Evidência: `.agents/state/iteracao.yaml` não contém `limite`
  - Status:

## Restrições

- Não quebrar compatibilidade com os demais agentes (questionador, explicador, validador) — eles não devem precisar de mudanças
- `docs/iteracao.md` (legado) deve continuar funcionando — manter compatibilidade
- Não remover funcionalidade existente do especulador (apenas adicionar)

## Resultado (preenchido no audit)

- [ ] Todos os critérios atendidos
