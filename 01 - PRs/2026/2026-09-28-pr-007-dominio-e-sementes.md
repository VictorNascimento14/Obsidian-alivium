---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 7
url: https://github.com/VictorNascimento14/Alivium/pull/7
branch: feat/dominio-e-sementes
tags: [pr, frontend, dados]
status: aberto
---

# PR #7 — feat(dados): tipos do domínio e conteúdo inicial

## 🎯 Contexto

Ordem 6 de [[2026-09-28-plano-da-v1-do-frontend]]. Primeira metade de
[[ADR-001-frontend-primeiro-com-dados-locais]].

## 🔧 Mudanças

- `src/dados/tipos.ts` — domínio; termos do [[glossario]].
- `src/dados/sementes.ts` — 6 categorias, 14 conteúdos, 4 jornadas, 2 contas de demonstração.

## 🕵️ Dado pessoal (LGPD)

Nenhum dado real: as contas de demonstração usam os exemplos estáveis (`Admin Exemplo`,
`Pessoa Exemplo`). Os tipos `CheckIn` e `EntradaDiario` **vão guardar dado emocional** a partir dos
PRs de check-in e diário — ficam só no navegador da pessoa.

## 🧠 Decisões técnicas

- Datas de calendário em `AAAA-MM-DD` local (`diaISO` do kit); `toISOString()` corta em UTC e jogaria
  o check-in das 22h para o dia seguinte.
- Um check-in por dia: registrar de novo substitui.
- Senha guardada como SHA-256 de `email + senha` — evita texto puro, **não** é segurança (não há
  servidor). Ver a ADR.
- Etapa aponta opcionalmente para um conteúdo: a jornada reusa a biblioteca em vez de duplicar texto.
- Corpo do conteúdo em parágrafos; linha iniciada por `• ` vira item de lista na leitura.

## 🧪 Como testar

1. `npm run type-check`.

## 📎 Documentação afetada

- [[CamadaDeDados]]
- [[glossario]]
- [[2026]] (changelog)
