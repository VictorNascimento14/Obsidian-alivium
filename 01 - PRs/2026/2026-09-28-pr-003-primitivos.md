---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 3
url: https://github.com/VictorNascimento14/Alivium/pull/3
branch: ui/primitivos
tags: [pr, frontend, design]
status: merged
---

# PR #3 — ui(primitivos): instalar os primitivos do vidro-orgânico

## 🎯 Contexto

Ordem 3 de [[2026-09-28-plano-da-v1-do-frontend]]. Segunda parte de
[[ADR-002-sistema-visual-vidro-organico]].

## 🔧 Mudanças

- `src/ui/base/*` — cópia literal do kit (13 primitivos).
- `src/ui/index.ts` — exporta os primitivos.
- `src/App.tsx` — vitrine provisória.

## 🕵️ Dado pessoal (LGPD)

Nenhum.

## 🧠 Decisões técnicas

- `Glyph` ainda tem só os 23 ícones do kit; os ícones de navegação do Alivium (livro, bússola, pena…)
  entram num PR próprio, no mesmo traçado 2.5.

## ⚠️ Armadilhas e aprendizados

- O `toast()` só aparece com o `ToastHost` montado — ele é da casca, próximo PR.

## 🧪 Como testar

1. `npm run dev`; conferir entrada escalonada, contagem e barra.

## 📎 Documentação afetada

- [[Primitivos]]
- [[2026]] (changelog)
