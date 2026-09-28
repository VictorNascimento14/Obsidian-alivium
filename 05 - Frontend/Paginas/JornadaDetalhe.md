---
tipo: funcionalidade
camada: frontend
area: Jornadas
rota: /jornadas/:id
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, jornadas, progresso]
---

# JornadaDetalhe

## O que é

A jornada aberta: cabeçalho com andamento e a linha do tempo das etapas. Vem de [[Jornadas]].

## Onde está no código

`src/paginas/jornadas/JornadaDetalhe.tsx`; regras em `src/dados/jornadas.ts`; [[AvisoApoio]] no pé.

## Comportamento

| Etapa | Visual | Botão |
|---|---|---|
| feita | círculo verde com ✓, cartão a 75% | "Feito" (desfaz) |
| próxima | anel + "Próximo passo", vidro médio | "Marcar como feito" (primário) |
| demais | número em pílula | "Marcar como feito" (fantasma) |

Etapa com conteúdo publicado mostra o link para a [[Leitura]].

## Movimento e micro-interações

Percentual com `AnimatedNumber`; barra com `bar-grow`; marcadores com `animate-pop` (remontam por
`key`); etapas com `rise` escalonado; cartão de celebração com emoji em `pop`.

## Histórico de mudanças

- [[2026-09-28-pr-017-jornada-detalhe]] — criada.
