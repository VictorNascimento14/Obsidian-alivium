---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 18
url: https://github.com/VictorNascimento14/Alivium/pull/18
branch: feat/inicio-continuar
tags: [pr, frontend, inicio]
status: merged
---

# PR #18 — feat(inicio): continuar jornada e conteúdos recomendados para o dia

## 🎯 Contexto

Ordem 12 de [[2026-09-28-plano-da-v1-do-frontend]] (feita depois das jornadas, que ela usa).

## 🔧 Mudanças

- `src/dados/recomendacoes.ts` (+ testes) — `recomendarConteudos`, `jornadaParaContinuar`.
- `src/paginas/inicio/Inicio.tsx` — coluna direita (continuar + frase) e seção "Para você hoje".

## 🕵️ Dado pessoal (LGPD)

Lê o check-in do dia para ordenar sugestões; nada novo é gravado.

## 🧠 Decisões técnicas

- Regra simples e explicável, sem "algoritmo": dia difícil → curto e prático primeiro. Cabe numa
  frase, então cabe numa nota de produto.
- Continuar = jornada em andamento iniciada mais recentemente.

## 🧪 Como testar

Ver [[Inicio]].

## 📎 Documentação afetada

- [[Inicio]]
- [[2026]] (changelog)
