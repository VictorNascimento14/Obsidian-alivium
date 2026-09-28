---
tipo: funcionalidade
camada: frontend
area: Comuns
rota: —
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, conteudos]
---

# ConteudoCard

## O que é

Cartão de um conteúdo, reusado na [[Biblioteca]] e, depois, no Início e nos salvos.

## Onde está no código

`src/componentes/ConteudoCard.tsx`; tons em `src/componentes/tons.ts`.

## Comportamento

Props: `conteudo`, `categoria`, `concluido`, `delay`, `envolver` (quem usa decide o link).

## Movimento e micro-interações

`GlassCard interactive sheen` (levanta e brilha); halo no tom da categoria; selo de concluído com
`animate-pop`.

## Histórico de mudanças

- [[2026-09-28-pr-013-biblioteca]] — criado.
