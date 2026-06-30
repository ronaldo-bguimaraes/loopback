# Lições Aprendidas

<!-- Acumuladas entre ciclos. Toda falha vira lição aqui. -->

## Ciclo 1
- Segurança: permissões irrestritas são risco — usar allowlists granulares
- Validação: quem implementa não deve validar (maker-checker split)
- Docs: toda etapa deve criar/atualizar ao menos um arquivo
- Iteração: usar contador em arquivo para controle entre ciclos
- Referências: todo arquivo mencionado deve existir antes de ser referenciado

## Ciclo 2
- Tool-agnostic: `.agents/` como fonte canônica, adaptadores como artefato
- Entry point: AGENTS.md na raiz é o padrão universal (30+ ferramentas)
- No-downgrade: políticas de segurança imutáveis entre ciclos

## Ciclo 3
- Spec first: todo ciclo deve começar com `docs/spec.md` (escrito pelo especulador)
- Audit mandatory: todo ciclo deve terminar com validação do especulador
- Especulador read-only previne auto-sabotagem (maker-checker split)

## Ciclo 4
- Ciclo enxuto de 5 passos é suficiente: spec → questionar → desenvolver → validar+melhorar → auditar
- Documentação como side-effect (contínua) funciona melhor que passo dedicado
- goal.md é redundante com spec.md — spec.md como fonte única simplifica
- Lessons.md deve ser consultado durante validação, não só no início

## Ciclo 6
- Preflight deve sempre definir `estimado` antes do ciclo começar — valor default 0 aciona avaliação prematuramente
- Chicken-and-egg: ao implementar feature do próprio ciclo, o preflight pode ser negligenciado; agendar execução explícita do preflight mesmo quando a mudança é no ciclo em si

## Ciclo 7
- State mutável compartilhado (`iteracao.yaml`, `goal.yaml`) reintroduz race conditions mesmo com ciclo-N/ imutável
- `goal.yaml` separado é redundante — `estimado` cabe no cabeçalho de `docs/spec.md`
- Todo estado mutável compartilhado = barril de pólvora — preferir append-only e snapshots imutáveis
- `mkdir` é atômico mas a contagem `ls | wc -l + 1` é vulnerável a races — documentar retry se falhar
- Questionador é essencial para detectar regressões na arquitetura (ex: goal.yaml reintroduziu o mesmo problema que estávamos resolvendo)

## Simplificação do Estado
- Controle fino de iterações (estimado, max, ciclo-N) era over-engineering — ninguém calibrava nem consultava
- O meio-termo entre "estrutura rígida" e "bagunça" é: critérios binários (qualidade) sem contagem numérica (quantidade)
- `memoria/` transitório + `lessons.md` versionado resolve o conflito entre estado descartável e conhecimento duradouro
- Loop guard (detecção de repetição) substitui hard limit numérico com mais precisão
- Questionador às vezes é conservador demais — importante ouvir mas também calibrar com o Explicador
