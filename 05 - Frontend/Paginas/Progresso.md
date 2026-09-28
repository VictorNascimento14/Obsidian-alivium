---
tipo: funcionalidade
camada: frontend
area: Progresso
rota: /progresso
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, progresso]
---

# Progresso

## O que é

O retrato do cuidado ao longo do tempo: indicadores, humor recente, dias de cuidado e jornadas.

## Onde está no código

`src/paginas/progresso/Progresso.tsx`; `src/dados/estatisticas.ts`.

## Comportamento

- Dia ativo = check-in, conteúdo concluído, etapa feita ou página do diário.
- Barras: 14 dias terminando hoje; altura = humor × 20%.

## Movimento e micro-interações

`StatCard` + `AnimatedNumber`; barras com `rise` em `stagger(i, 35)`; `MeterBar` com `bar-grow`.

## Histórico de mudanças

- [[2026-09-28-pr-020-progresso]] — criada.
