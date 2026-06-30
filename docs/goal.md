# Goal — Ciclo 3

## Estado desejado
Agente especulador que define specs antes do ciclo e valida depois,
integrado no fluxo loopback.

## Evidências
- `.agents/agents/especulador.md` existe com modos preflight e audit
- `.agents/agents/loopback.md` referencia especulador nos passos 0 e 7
- `opencode.json` registra especulador

## Restrições
- Especulador não deve ter permissão de escrita (read-only)

## Critérios de parada
- [x] Agente criado
- [x] Integrado no ciclo
- [x] Registrado no opencode.json
