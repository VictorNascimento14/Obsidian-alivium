---
tipo: funcionalidade
camada: frontend
area: Diario
rota: /diario
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, diario, progresso]
---

# Diário

## O que é

Reflexões livres com um humor associado. Termo no [[glossario]].

## Onde está no código

`src/paginas/diario/Diario.tsx`; regras em `src/dados/diario.ts`; [[AvisoApoio]] no pé.

## Comportamento

| Regra | Valor |
|---|---|
| Texto | obrigatório, até 5.000 |
| Título | opcional, até 80; vazio vira "Sem título" |
| Humor | 1–5 |
| Editar / apagar | só a dona da entrada; apagar pede confirmação |

## Movimento e micro-interações

Humor com `scale-110` + anel no escolhido (`duration-open ease-organic`); sugestões em pílula com
`.press`; entradas com `rise` escalonado e `.lift`; modal do kit (cortina + vidro forte).

## Histórico de mudanças

- [[2026-09-28-pr-019-diario]] — criada.
