---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 16
url: https://github.com/VictorNascimento14/Alivium/pull/16
branch: feat/jornadas-lista
tags: [pr, frontend, jornadas]
status: merged
---

# PR #16 — feat(jornadas): lista de jornadas com andamento

## 🎯 Contexto

Ordem 16 de [[2026-09-28-plano-da-v1-do-frontend]]. Funcionalidade 4 de [[visao-de-produto]].

## 🔧 Mudanças

- `src/paginas/jornadas/Jornadas.tsx`, `src/componentes/JornadaCard.tsx`.
- `src/dados/jornadas.ts` (+ testes); `mexerProgresso` em `repositorio.ts`.
- `navegacao.tsx`, `App.tsx`.

## 🕵️ Dado pessoal (LGPD)

Estrutura para gravar etapas feitas e jornadas iniciadas (a escrita começa no próximo PR).

## 🧠 Decisões técnicas

- "Próxima etapa" = primeira não feita **na ordem da jornada**, mesmo que a pessoa tenha pulado — a
  jornada não obriga ordem, mas sugere.
- Marcar uma etapa dá a jornada por iniciada; desmarcar não "desinicia".
- Ordem dos grupos: em andamento primeiro (onde a pessoa quer voltar).

## 🧪 Como testar

Ver [[Jornadas]].

## 📎 Documentação afetada

- [[Jornadas]]
- [[JornadaCard]]
- [[CamadaDeDados]]
- [[2026]] (changelog)
