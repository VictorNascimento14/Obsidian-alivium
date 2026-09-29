---
tipo: funcionalidade
camada: frontend
area: Administracao
rota: /admin/categorias
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, admin]
---

# Administração — Categorias

## O que é

CRUD das categorias que organizam a [[Biblioteca]].

## Onde está no código

`src/paginas/admin/AdminCategorias.tsx`; regras em `src/dados/catalogo.ts`; [[SeletoresDoCatalogo]].

## Comportamento

| Regra | Valor |
|---|---|
| Nome | 2–40, único sem diferenciar caixa |
| Descrição | até 140 |
| Ícone | classe Remix `ri-…` da lista |
| Apagar | só sem conteúdo |

## Movimento e micro-interações

Linhas com `rise` escalonado; prévia com ícone em `pop` (remonta por `key`); tom escolhido com
`scale-110` + anel e ✓ em `pop`.

## Histórico de mudanças

- [[2026-09-28-pr-024-admin-categorias]] — criada.
