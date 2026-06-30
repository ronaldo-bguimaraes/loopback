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
