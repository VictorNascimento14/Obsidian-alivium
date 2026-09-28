---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 1
url: https://github.com/VictorNascimento14/Alivium/pull/1
branch: chore/scaffolding
tags: [pr, infra, scaffolding]
status: merged
---

# PR #1 — chore: scaffolding Vite + React + TypeScript + ESLint

## 🎯 Contexto

Primeiro PR de código da v1 ([[2026-09-28-plano-da-v1-do-frontend]], ordem 1). Cria o esqueleto em cima
do qual o sistema visual entra.

## 🔧 Mudanças

- `package.json`, `vite.config.ts`, `tsconfig*.json`, `eslint.config.js` — vindos do `template/` do
  kit vidro-orgânico, sem as dependências do Tailwind (entram no PR da fundação visual).
- `index.html` com `lang="pt-BR"` e título do produto.
- `src/App.tsx` mínimo.

## 🕵️ Dado pessoal (LGPD)

Nenhum.

## 🧠 Decisões técnicas

- **Vite em vez de Next.js**: a v1 é só front-end, sem SSR nem rota de servidor
  ([[ADR-001-frontend-primeiro-com-dados-locais]]); o kit foi feito para Vite.
- `build.outDir = out` e `BASE_PATH` opcional — herdados do template, permitem deploy em subpasta.

## 🧪 Como testar

1. `npm install`
2. `npm run lint && npm run type-check && npm run build`
3. `npm run dev` → `http://localhost:3000`

## 📎 Documentação afetada

- [[runbook-rodar-local]]
- [[2026]] (changelog)
