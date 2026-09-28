---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 17
url: https://github.com/VictorNascimento14/Alivium/pull/17
branch: feat/jornada-detalhe
tags: [pr, frontend, jornadas, progresso]
status: merged
---

# PR #17 — feat(jornadas): detalhe da jornada com etapas e próximo passo

## 🎯 Contexto

Ordem 17 de [[2026-09-28-plano-da-v1-do-frontend]]. Completa a funcionalidade 4 de
[[visao-de-produto]].

## 🔧 Mudanças

- `src/paginas/jornadas/JornadaDetalhe.tsx` — página.
- `Jornadas.tsx` — cartões com link; `App.tsx` — rota.

## 🕵️ Dado pessoal (LGPD)

Grava quando cada etapa foi feita e quando a jornada começou, por pessoa, no `localStorage`.

## 🧠 Decisões técnicas

- O aviso de conclusão relê o estado com `lerEstado()` logo após a escrita — o `estado` do render ainda
  é o anterior.
- Etapas podem ser feitas fora de ordem; o destaque de "próximo passo" só sugere.
- Marcadores remontam por `key` (feita/aberta) para o `pop` tocar na troca.

## 🧪 Como testar

Ver [[JornadaDetalhe]].

## 📎 Documentação afetada

- [[JornadaDetalhe]]
- [[Jornadas]]
- [[2026]] (changelog)
