---
tipo: funcionalidade
camada: frontend
area: Shell
rota: todas as telas logadas
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, shell]
---

# Casca (coluna, cabeçalho, barra do celular)

## O que é

A moldura das telas logadas, vinda do kit ([[SistemaVisual]], [[Primitivos]]).

## Onde está no código

- `src/ui/shell/` — componentes do kit.
- `src/navegacao.tsx` — **o único arquivo que muda** quando entra uma área nova: grupos da coluna e
  `BARRA_CELULAR` (até 5 destinos, na ordem do celular).
- `src/App.tsx` — rotas; toda tela com coluna é filha do `RailLayout`.

## Comportamento

- Coluna 76 px (recolhida) ↔ 236 px (aberta), flutuando a 16 px da borda; conteúdo desloca por CSS
  (`html[data-rail]`).
- Clicar num item só desliza o marcador — a coluna não recolhe nem pisca.
- Abaixo de `md`: gaveta pelo botão de menu + barra de baixo.

## Movimento e micro-interações

Marcador que desliza (conta, não medida), espiada por hover, `.press` nos botões, entrada `rise` das
páginas.

## Histórico de mudanças

- [[2026-09-28-pr-005-casca]] — casca instalada, com Início.
- [[2026-09-28-pr-013-biblioteca]] — item Conteúdos na coluna e na barra do celular.
- [[2026-09-28-pr-016-jornadas-lista]] — item Jornadas na coluna e na barra.
- [[2026-09-28-pr-019-diario]] — item Diário na coluna e na barra.
