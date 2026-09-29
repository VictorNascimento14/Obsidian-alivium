---
tipo: funcionalidade
camada: frontend
area: Conteudos
rota: /conteudos/:id (tipo respiração)
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, conteudos]
---

# GuiaDeRespiracao

## O que é

Prática guiada de respiração na [[Leitura]]: círculo que cresce (inspirar) e encolhe (soltar).

## Onde está no código

`src/componentes/GuiaDeRespiracao.tsx`; props `inspirar` e `soltar` em segundos (padrão 4 e 6).

## Movimento e micro-interações

`transform: scale` com `transition` igual à duração da fase (`ease-in-out`); anel tracejado de
referência; instrução em `aria-live="polite"`. Movimento reduzido: sem escala.

## Histórico de mudanças

- [[2026-09-28-pr-028-guia-respiracao]] — criado.
