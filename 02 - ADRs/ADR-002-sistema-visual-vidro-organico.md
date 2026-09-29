---
tipo: adr
numero: 2
data: 2026-09-28
status: aceito
tags: [adr, design, frontend]
---

# ADR-002 — Sistema visual vidro-orgânico, instalado sem alteração

## Contexto

O dono entregou o kit **vidro-orgânico** como design e pediu o app "exatamente com esse layout",
incluindo animações e micro-interações.

## Decisão

- O kit é copiado para `src/ui/` e **não é alterado** para acertar uma tela.
- Telas com coluna lateral são filhas do `RailLayout` e passam pelo `PageShell`.
- Telas de autenticação (entrar, cadastro) ficam **fora** do `RailLayout` — não há coluna antes da
  sessão existir — mas usam os mesmos primitivos (`GlassCard`, `TextField`, `Button`).
- Ícones: `Glyph` na navegação e nas pastilhas de indicador; Remix Icon no resto.

## Consequências

- Mudança de rampa em `src/ui/index.css` repinta o app inteiro — é a alavanca certa só para
  retonalizar a marca, nunca para uma tela.
- Ícones novos de navegação são `path`s acrescentados ao `Glyph`, no mesmo traçado 2.5.

## Implementado em

- [[2026-09-28-pr-002-fundacao-visual]] · [[2026-09-28-pr-003-primitivos]] · [[2026-09-28-pr-004-icones]] · [[2026-09-28-pr-005-casca]]
- Correções no kit feitas aqui: [[2026-09-28-pr-011-icone-do-campo]], [[2026-09-28-pr-021-calendario-mes]] — ver [[2026-09-28-levar-correcoes-ao-kit]].
