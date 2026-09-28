---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 8
url: https://github.com/VictorNascimento14/Alivium/pull/8
branch: feat/repositorio-local
tags: [pr, frontend, dados]
status: merged
---

# PR #8 — feat(dados): repositório local com persistência e testes

## 🎯 Contexto

Ordem 7 de [[2026-09-28-plano-da-v1-do-frontend]]. Completa
[[ADR-001-frontend-primeiro-com-dados-locais]].

## 🔧 Mudanças

- `src/dados/repositorio.ts` — `lerEstado`, `atualizar`, `assinar`, `useEstado`, `restaurarSementes`,
  `progressoDe`, `novoId`, `agora`.
- `src/dados/repositorio.test.ts` — 6 verificações.
- `package.json` — `vitest` e script `test`; `ci.yml` roda `npm test`.
- `CLAUDE.md` — checks passam a ser quatro.

## 🕵️ Dado pessoal (LGPD)

A partir daqui, o que o app gravar fica em `localStorage` sob `alivium-dados-v1`, **só neste
navegador**. Nada sai da máquina.

## 🧠 Decisões técnicas

- **Hook devolve o estado inteiro, não um seletor.** Seletor que cria objeto novo a cada chamada faz o
  `useSyncExternalStore` renderizar em laço; derivar com `useMemo` na tela é seguro.
- **API síncrona**: com tudo em memória, nenhuma tela precisa de "carregando" para ler.
- `novoId` tem plano B para `crypto.randomUUID`, que só existe em contexto seguro — abrir o app pelo IP
  da rede local (`http://192.168…`) quebraria sem ele.
- Vitest em ambiente `node`, sem jsdom: o repositório tolera a ausência de `localStorage`, e isso
  mantém a dependência pequena.

## ⚠️ Armadilhas e aprendizados

- Escrita que muta o estado em vez de devolver um novo não re-renderiza ninguém — o comentário em
  `atualizar` diz isso.

## 🧪 Como testar

1. `npm test` — 6 verificações verdes.

## 📎 Documentação afetada

- [[CamadaDeDados]]
- [[runbook-ci]]
- [[2026]] (changelog)
