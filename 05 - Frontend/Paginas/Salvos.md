---
tipo: funcionalidade
camada: frontend
area: Conteudos
rota: /salvos
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, conteudos]
---

# Salvos

## O que é

Os conteúdos que a pessoa guardou pelo coração da [[Leitura]].

## Onde está no código

`src/paginas/conteudos/Salvos.tsx`; `alternarSalvo` em `src/dados/progresso.ts`.

## Comportamento

Mais recente primeiro; só publicados; estado vazio com link para a [[Biblioteca]].

## Movimento e micro-interações

Coração com `animate-pop` a cada toque (remonta por `key`); cartões com `rise` escalonado; ícone do
estado vazio com `pop`.

## Histórico de mudanças

- [[2026-09-28-pr-015-salvos]] — criada.
