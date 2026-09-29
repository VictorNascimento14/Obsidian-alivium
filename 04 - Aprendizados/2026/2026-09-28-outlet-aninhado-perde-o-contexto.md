---
tipo: aprendizado
data: 2026-09-28
contexto: PR #23
tags: [aprendizado, react-router, shell]
---

# `<Outlet />` aninhado perde o contexto do `RailLayout`

## O sintoma

No [[PainelAdmin]], o cabeçalho apareceu só com o botão de tema — sem a conta e sem "Sair".

## A causa

`useOutletContext()` lê o contexto do `<Outlet>` **mais próximo**. A rota `/admin` tinha um
`<Outlet />` próprio (para a guarda), sem `context` — e as telas de baixo recebiam `undefined`. O
`PageShell` trata isso como "tela sem coluna" e monta o cabeçalho sem conta.

## A correção

A guarda `RotaAdmin` lê o contexto de cima e repassa: `<Outlet context={useOutletContext()} />`
([[2026-09-28-pr-023-admin-painel]]).

## Como evitar

Toda rota de layout intermediária abaixo do `RailLayout` repassa o contexto. Sintoma a procurar:
cabeçalho sem conta numa tela com coluna.
