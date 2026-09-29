---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 29
url: https://github.com/VictorNascimento14/Alivium/pull/29
branch: chore/icone-e-manifesto
tags: [pr, frontend, infra]
status: aberto
---

# PR #29 — chore(pwa): ícone, manifesto e metadados do app

## 🎯 Contexto

Ordem 26 de [[2026-09-28-plano-da-v1-do-frontend]].

## 🔧 Mudanças

- `public/favicon.svg`, `public/manifest.webmanifest`, `index.html`.

## 🕵️ Dado pessoal (LGPD)

Nenhum.

## 🧠 Decisões técnicas

- Ícone em SVG único (`sizes: any`) em vez de vários PNG: sem dependência de ferramenta de imagem.
  ponytail: o iOS ignora SVG no "Adicionar à Tela de Início" — se isso importar, gerar um PNG 180×180.
- Sem service worker: offline não foi pedido, e o dado já vive no navegador.

## 🧪 Como testar

Aba com a folha; console limpo.

## 📎 Documentação afetada

- [[2026]] (changelog)
