---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 23
url: https://github.com/VictorNascimento14/Alivium/pull/23
branch: feat/admin-painel
tags: [pr, frontend, admin]
status: aberto
---

# PR #23 — feat(admin): painel administrativo com métricas agregadas e guarda de papel

## 🎯 Contexto

Ordem 21 de [[2026-09-28-plano-da-v1-do-frontend]]. Funcionalidade 6 de [[visao-de-produto]].

## 🔧 Mudanças

- `src/paginas/admin/PainelAdmin.tsx`.
- `src/dados/admin.ts` (+ teste) — `metricas`.
- `src/sessao/Guardas.tsx` — `RotaAdmin` (rota de layout).
- `src/navegacao.tsx` — `GRUPO_ADMIN`, `gruposPara`; `LayoutLogado.tsx` usa por papel.

## 🕵️ Dado pessoal (LGPD)

A administração vê **contagens e médias**, nunca registro de uma pessoa. O teste garante que nenhum id
de pessoa aparece na saída de `metricas`.

## 🧠 Decisões técnicas

- `gruposPara` devolve a mesma referência por papel — lista nova a cada render refaria o contexto do
  `RailLayout`.
- A guarda é rota de layout (`element: <RotaAdmin />` com filhos), não componente envolvendo cada tela.

## ⚠️ Armadilhas e aprendizados

- [[2026-09-28-outlet-aninhado-perde-o-contexto]]

## 🧪 Como testar

Ver [[PainelAdmin]].

## 📎 Documentação afetada

- [[PainelAdmin]]
- [[GuardasDeSessao]]
- [[Casca]]
- [[2026]] (changelog)
