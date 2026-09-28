---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 11
url: https://github.com/VictorNascimento14/Alivium/pull/11
branch: fix/icone-do-campo
tags: [pr, frontend, design, bug]
status: aberto
---

# PR #11 — fix(ui): ícone do TextField ficava escondido atrás do campo

## 🎯 Contexto

Descoberto ao conferir [[Cadastro]] por screenshot ampliado: o ícone dos campos virava um borrão.

## 🔧 Mudanças

- `src/ui/base/TextField.tsx` — `z-10` + `pointer-events-none` no ícone.

## 🕵️ Dado pessoal (LGPD)

Nenhum.

## 🧠 Decisões técnicas

- Correção no primitivo, não na tela: o bug é do componente e aparece em todo campo com ícone.
- **Divergência com o kit**: o `vidro-organico` tem o mesmo bug. A correção precisa ser levada lá à
  mão (relação de cópia, não de dependência). TODO: abrir o PR no repositório do kit.

## ⚠️ Armadilhas e aprendizados

- [[2026-09-28-backdrop-filter-pinta-por-cima-do-icone]]

## 🧪 Como testar

1. Tema escuro, `/cadastro`: ícones nítidos.

## 📎 Documentação afetada

- [[Primitivos]]
- [[2026-09-28-backdrop-filter-pinta-por-cima-do-icone]]
- [[2026]] (changelog)
