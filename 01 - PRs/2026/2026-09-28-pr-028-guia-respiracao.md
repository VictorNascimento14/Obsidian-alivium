---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 28
url: https://github.com/VictorNascimento14/Alivium/pull/28
branch: feat/guia-respiracao
tags: [pr, frontend, conteudos]
status: aberto
---

# PR #28 — feat(conteudos): guia animado de respiração

## 🎯 Contexto

Ordem extra do [[2026-09-28-plano-da-v1-do-frontend]]: prática guiada para o tipo respiração da
[[Leitura]].

## 🔧 Mudanças

- `src/componentes/GuiaDeRespiracao.tsx`.
- `Leitura.tsx` — mostra o guia quando `tipo === "respiracao"`.

## 🕵️ Dado pessoal (LGPD)

Nenhum.

## 🧠 Decisões técnicas

- A duração da transição (4 s/6 s) é **tempo da respiração**, conteúdo — não entra no vocabulário
  fechado de movimento do kit (`--dur-*`), e por isso fica em `style`.
- Um estado único `{ fase, resta, ciclos }`: efeito colateral dentro de atualizador de estado roda duas
  vezes no StrictMode e contaria ciclos em dobro.
- `usePrefersReducedMotion` do kit: movimento em JS consulta o hook (a fundação só anula o CSS).

## 🧪 Como testar

Ver [[GuiaDeRespiracao]].

## 📎 Documentação afetada

- [[GuiaDeRespiracao]]
- [[Leitura]]
- [[2026]] (changelog)
