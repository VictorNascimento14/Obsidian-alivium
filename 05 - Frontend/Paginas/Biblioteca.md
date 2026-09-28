---
tipo: funcionalidade
camada: frontend
area: Conteudos
rota: /conteudos
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, conteudos]
---

# Biblioteca

## O que é

Os conteúdos publicados, organizados por categoria.

## Onde está no código

`src/paginas/conteudos/Biblioteca.tsx`; cartão [[ConteudoCard]].

## Comportamento

| Filtro | Parâmetro | Regra |
|---|---|---|
| Categoria | `categoria` | id da categoria; vazio = todas |
| Tipo | `tipo` | leitura, reflexão, prática, respiração |
| Busca | `q` | título + resumo, sem acento e sem caixa |

Só conteúdos com `publicado: true`. Estado vazio quando nada casa.

## Movimento e micro-interações

Pílulas com `.press`; ativa em `bg-primary-900` com `shadow-nav-active`; cartões com `rise` em
`stagger(i, 60)`; select desdobra pelo `::picker(select)` do kit.

## Histórico de mudanças

- [[2026-09-28-pr-013-biblioteca]] — criada.
