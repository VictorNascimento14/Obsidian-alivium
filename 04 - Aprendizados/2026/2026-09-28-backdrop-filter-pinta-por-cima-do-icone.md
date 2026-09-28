---
tipo: aprendizado
data: 2026-09-28
contexto: PR #11
tags: [aprendizado, css, design]
---

# `backdrop-filter` pinta por cima do ícone posicionado

## O sintoma

Ícone à esquerda dos campos (`TextField`) aparecia como um quadrado escuro borrado — quase invisível no
tema escuro.

## A causa

`backdrop-filter` (o `backdrop-blur` do Tailwind) cria um **contexto de empilhamento**. Na pintura, um
elemento com contexto de empilhamento e `z-index: auto` entra na mesma camada dos elementos
posicionados, **em ordem de DOM**. O ícone (`absolute`) vinha antes do `<input>` no DOM; o input, com
o blur, pintava depois — por cima.

## A correção

`z-10` no ícone ([[2026-09-28-pr-011-icone-do-campo]]). `pointer-events-none` junto, para o clique atravessar até o campo.

## Como evitar

Todo elemento decorativo `absolute` sobre um irmão com `backdrop-filter`, `filter`, `opacity < 1` ou
`transform` precisa de `z-index` explícito — não confie na ordem "posicionado pinta por cima".
