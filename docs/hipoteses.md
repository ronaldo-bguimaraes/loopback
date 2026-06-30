# Hipóteses — Simplificação do Estado

## Tensão identificada

- **Questionador**: remover controle = repetir erros passados (loops, perda de contexto)
- **Explicador**: over-engineering real, indústria converge para estado flat

## Meio-termo

| O que | Decisão | Por quê |
|-------|---------|---------|
| `ciclo-N/` | Remove → `memoria/` com `.md` livres | Narrativa > hierarquia numérica |
| `estimado` / `max` | Remove | Nunca foi calibrado; agente+usuário decidem quando parar |
| `avaliacao.md` | Remove | Nunca foi lido |
| Critérios binários | **Mantém** | Essencial para quality gate no passo 4-5 |
| `lessons.md` | **Mantém versionado** | Conhecimento duradouro — não pode ser transitório |
| `memoria/` | `.gitignore` | Transitório por natureza |
| Loop guard | Adiciona substituto leve | 3 ciclos com o mesmo spec → alerta |
