---
tipo: funcionalidade
camada: frontend
area: Jornadas
rota: /jornadas
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, jornadas]
---

# Jornadas

## O que é

Lista das jornadas publicadas, agrupadas pela situação de quem está vendo.

## Onde está no código

`src/paginas/jornadas/Jornadas.tsx`; [[JornadaCard]]; regras em `src/dados/jornadas.ts`.

## Comportamento

Grupos: Em andamento → Para começar → Concluídas (grupo vazio não aparece).

## Movimento e micro-interações

Cartões com `rise` em `stagger(i, 70)` contínuo entre grupos; selo "em andamento" com `animate-live`;
barra com `bar-grow`.

## Histórico de mudanças

- [[2026-09-28-pr-016-jornadas-lista]] — criada.
- [[2026-09-28-pr-017-jornada-detalhe]] — cartões viram links para o detalhe.
