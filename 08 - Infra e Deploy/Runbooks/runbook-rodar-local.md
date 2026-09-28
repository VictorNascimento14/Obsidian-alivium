---
tipo: runbook
camada: frontend
escopo: rodar o app na máquina
ultima_atualizacao: 2026-09-28
tags: [runbook, frontend]
tempo_estimado: 2 min
---

# Runbook — rodar o Alivium local

## Quando usar

Primeira vez numa máquina, ou depois de trocar de branch com `package.json` diferente.

## Passos

1. `cd "$ALIVIUM_REPO"`
2. `npm install`
3. `npm run dev` — sobe em `http://localhost:3000` (também na rede local: `0.0.0.0`).

Checks que o CI roda: `npm run lint && npm run type-check && npm run build`.

## Como saber que deu certo

A página abre sem erro no console. Criado em [[2026-09-28-pr-001-scaffolding]].
