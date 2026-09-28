---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 2
url: https://github.com/VictorNascimento14/Alivium/pull/2
branch: ui/fundacao-visual
tags: [pr, frontend, design]
status: merged
---

# PR #2 — ui(fundacao): instalar a fundação do sistema vidro-orgânico

## 🎯 Contexto

Ordem 2 de [[2026-09-28-plano-da-v1-do-frontend]]. Implementa a parte de fundação de
[[ADR-002-sistema-visual-vidro-organico]].

## 🔧 Mudanças

- `src/ui/index.css`, `tailwind.config.ts`, `postcss.config.ts` — cópia literal do kit.
- `src/ui/lib/{motion,data,tema,sidebarCollapsed,toast}.ts`, `src/ui/hooks/useInView.ts`.
- `src/ui/lib/marca.ts` — `SLUG = "alivium"`, `NOME = "Alivium"`, `MONOGRAMA = "A"`.
- `src/ui/index.ts` — barril só com a fundação; primitivos e casca entram nos PRs seguintes.
- `index.html` — script do tema lendo `alivium-tema` antes da primeira pintura.

## 🕵️ Dado pessoal (LGPD)

Nenhum. O `localStorage` guarda só preferência de tema.

## 🧠 Decisões técnicas

- O barril `@/ui` cresce PR a PR, em vez de chegar inteiro, para cada PR compilar sozinho.
- O prefixo da chave do tema no `index.html` tem de bater com o `SLUG` — se a marca mudar, os dois
  mudam juntos.

## ⚠️ Armadilhas e aprendizados

- `animation-fill-mode` é `backwards`, nunca `both`: com `both` o último quadro congela o `transform` e
  anula o `:hover` do `.lift`. A tela provisória usa `.lift` + `rise` juntos justamente para provar isso.

## 🧪 Como testar

1. `npm run dev`; os cartões entram em sequência.
2. Hover no segundo: levanta e passa o brilho diagonal.

## 📎 Documentação afetada

- [[SistemaVisual]]
- [[linguagem-visual]]
- [[2026]] (changelog)
