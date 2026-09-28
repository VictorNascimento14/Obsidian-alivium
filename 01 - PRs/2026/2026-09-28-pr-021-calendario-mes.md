---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 21
url: https://github.com/VictorNascimento14/Alivium/pull/21
branch: fix/calendario-mes
tags: [pr, frontend, design, bug]
status: aberto
---

# PR #21 — fix(ui): mês do calendário com só a primeira letra maiúscula

## 🎯 Contexto

Resolve [[2026-09-28-calendar-capitaliza-cada-palavra]], vista em [[Progresso]].

## 🔧 Mudanças

- `src/ui/base/Calendar.tsx` — `first-letter:uppercase` + `inline-block`.

## 🕵️ Dado pessoal (LGPD)

Nenhum.

## 🧠 Decisões técnicas

- Correção no primitivo (o erro é do componente). O kit vidro-orgânico tem o mesmo defeito — levar à
  mão, junto com o do [[2026-09-28-backdrop-filter-pinta-por-cima-do-icone]].

## 🧪 Como testar

Progresso → "Setembro de 2026".

## 📎 Documentação afetada

- [[Primitivos]]
- [[2026]] (changelog)
