---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 24
url: https://github.com/VictorNascimento14/Alivium/pull/24
branch: feat/admin-categorias
tags: [pr, frontend, admin, conteudos]
status: merged
---

# PR #24 — feat(admin): gerenciar categorias do catálogo

## 🎯 Contexto

Ordem 22 de [[2026-09-28-plano-da-v1-do-frontend]]. Funcionalidade 6 de [[visao-de-produto]].

## 🔧 Mudanças

- `src/paginas/admin/AdminCategorias.tsx`, `src/paginas/admin/Seletores.tsx`.
- `src/dados/catalogo.ts` (+ testes).
- `navegacao.tsx` (item Categorias no grupo Administração), `App.tsx`.

## 🕵️ Dado pessoal (LGPD)

Nenhum: catálogo não é dado de pessoa.

## 🧠 Decisões técnicas

- Ícone validado por padrão (`ri-…`), não texto livre: o valor vira classe CSS na tela.
- Categoria com conteúdo não se apaga — "mover antes" é explícito, nada some em cascata sem querer.
- Um modal só para criar e editar (`id` ausente = criando).

## 🧪 Como testar

Ver [[AdminCategorias]].

## 📎 Documentação afetada

- [[AdminCategorias]]
- [[SeletoresDoCatalogo]]
- [[2026]] (changelog)
