---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 12
url: https://github.com/VictorNascimento14/Alivium/pull/12
branch: feat/inicio-checkin
tags: [pr, frontend, inicio]
status: merged
---

# PR #12 — feat(inicio): saudação personalizada e check-in de humor e dor

## 🎯 Contexto

Ordem 11 de [[2026-09-28-plano-da-v1-do-frontend]]. Funcionalidades 2 e 5 de [[visao-de-produto]].

## 🔧 Mudanças

- `src/paginas/inicio/Inicio.tsx` — saudação, intenção, grade com check-in e frase do dia.
- `src/paginas/inicio/CheckInCard.tsx` — formulário ↔ resumo.
- `src/paginas/inicio/frases.ts` — `saudacao`, `fraseDoDia`.
- `src/dados/checkins.ts` (+ testes) — `registrarCheckin`, `checkinDoDia`, `checkinsDe`.

## 🕵️ Dado pessoal (LGPD)

**Primeiro dado emocional gravado**: humor e dor do dia, por pessoa, no `localStorage`. Não sai do
navegador.

## 🧠 Decisões técnicas

- Um check-in por dia (substitui) — é um retrato, não um log; o histórico diário alimenta o progresso.
- A resposta ao registro acolhe e não corrige; o CVV aparece só quando o registro pede (humor 1 ou dor
  ≥ 9), para não banalizar o aviso.
- Validação de faixa em `src/dados/` (humor 1–5 lança erro; dor presa em 0–10).
- Verificado de ponta a ponta no navegador (login pela UI, check-in, resumo) nos dois temas.

## 🧪 Como testar

Ver [[Inicio]] e [[CheckInCard]].

## 📎 Documentação afetada

- [[Inicio]]
- [[CheckInCard]]
- [[2026]] (changelog)
