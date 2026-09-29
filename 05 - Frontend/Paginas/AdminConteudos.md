---
tipo: funcionalidade
camada: frontend
area: Administracao
rota: /admin/conteudos · /admin/conteudos/:id
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, admin, conteudos]
---

# Administração — Conteúdos

## O que é

Lista e editor dos conteúdos da [[Biblioteca]].

## Onde está no código

`src/paginas/admin/AdminConteudos.tsx` (lista) e `EditorConteudo.tsx` (`novo` ou id); regras em
`src/dados/catalogo.ts`; prévia com [[CorpoDoConteudo]].

## Comportamento

| Regra | Valor |
|---|---|
| Título | 3–90 |
| Resumo | 10–160 |
| Minutos | 1–120 (inteiro) |
| Corpo | ao menos um parágrafo |
| Publicar | interruptor na lista ou caixa no editor |
| Apagar | confirma; solta etapas de jornada |

## Movimento e micro-interações

Interruptor (`role="switch"`) com bola deslizando e cor em `duration-open ease-organic`; linhas com
`rise`; título com `.underline-grow`; prévia grudada ao rolar no desktop.

## Histórico de mudanças

- [[2026-09-28-pr-025-admin-conteudos]] — criada.
