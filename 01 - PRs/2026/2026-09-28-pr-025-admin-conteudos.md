---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 25
url: https://github.com/VictorNascimento14/Alivium/pull/25
branch: feat/admin-conteudos
tags: [pr, frontend, admin, conteudos]
status: aberto
---

# PR #25 — feat(admin): gerenciar conteúdos com editor e prévia ao vivo

## 🎯 Contexto

Ordem 23 de [[2026-09-28-plano-da-v1-do-frontend]]. Funcionalidade 6 de [[visao-de-produto]].

## 🔧 Mudanças

- `src/paginas/admin/AdminConteudos.tsx`, `src/paginas/admin/EditorConteudo.tsx`.
- `src/componentes/CorpoDoConteudo.tsx` (extraído de `Leitura.tsx`).
- `src/dados/catalogo.ts` — conteúdos (+ testes).
- `navegacao.tsx`, `App.tsx`.

## 🕵️ Dado pessoal (LGPD)

Nenhum.

## 🧠 Decisões técnicas

- Corpo editado como texto simples, não editor rico: o formato do domínio (parágrafos + itens "• ")
  cabe em duas regras, e `corpoDeTexto(textoDeCorpo(x)) === x` está testado.
- Apagar conteúdo **solta** a etapa de jornada (tira o `conteudoId`) em vez de apagar a etapa —
  jornada de quem já estava no meio não perde passo.
- O editor lê o conteúdo uma vez na montagem; a partir daí o formulário é dono do rascunho.
- Uma rota `conteudos/:id` para "novo" e edição.

## 🧪 Como testar

Ver [[AdminConteudos]].

## 📎 Documentação afetada

- [[AdminConteudos]]
- [[CorpoDoConteudo]]
- [[Leitura]]
- [[2026]] (changelog)
