---
tipo: adr
numero: 1
data: 2026-09-28
status: aceito
tags: [adr, arquitetura, dados]
---

# ADR-001 — Front-end primeiro, com dados locais atrás de uma fronteira

## Contexto

O dono pediu **apenas o front-end** da v1. Ainda assim o produto precisa de cadastro, login,
progresso e uma área administrativa que edita conteúdo — tudo isso pressupõe estado persistente.

## Decisão

1. Toda leitura e escrita de dado passa por **`src/dados/`**: tipos do domínio, sementes e um
   repositório com API síncrona.
2. A persistência da v1 é o **`localStorage`** do navegador, com chave prefixada pelo `SLUG` da marca.
3. Componentes **nunca** tocam `localStorage` direto; assinam o repositório via
   `useSyncExternalStore`.
4. A "autenticação" da v1 é local: cadastro guarda o usuário no repositório, login confere e-mail e
   senha lá. **Não é segurança** — é o formato do fluxo, para a tela existir.

## Consequências

- ✅ Trocar por backend real mexe em `src/dados/` e não nas telas.
- ✅ A área admin edita o mesmo repositório que as telas leem — dá para ver a edição refletida.
- ⚠️ Senha em `localStorage` é aceitável **só** porque não existe servidor; a v1 avisa isso na tela de
  cadastro. Quando houver backend, a senha sai do cliente por completo.
- ⚠️ Dado de um navegador não aparece em outro.

## Implementado em

TODO: linkar os PRs da camada de dados quando mergearem.
