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
