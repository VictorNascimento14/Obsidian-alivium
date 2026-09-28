---
tipo: funcionalidade
camada: frontend
area: Inicio
rota: /
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, inicio, progresso]
---

# CheckInCard

## O que é

Registro rápido de humor (1–5) e dor (0–10) do dia. Termo no [[glossario]].

## Onde está no código

`src/paginas/inicio/CheckInCard.tsx`; dados em `src/dados/checkins.ts`.

## Comportamento

| Estado | O que mostra |
|---|---|
| sem check-in hoje | 5 humores + régua de dor + "Registrar" (desabilitado sem humor) |
| com check-in | resumo (emoji, rótulo, dor, hora) + resposta acolhedora + "Atualizar" |
| humor 1 ou dor ≥ 9 | + aviso do CVV 188 |

## Movimento e micro-interações

Humores com `animate-pop` escalonado (`stagger(i, 60)`), `.press`, emoji `scale-125` no escolhido
(`duration-open ease-organic`); troca formulário↔resumo com `fade-up`; emoji do resumo com `pop`.

## Histórico de mudanças

- [[2026-09-28-pr-012-inicio-checkin]] — criado.
