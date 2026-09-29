---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 26
url: https://github.com/VictorNascimento14/Alivium/pull/26
branch: feat/admin-jornadas
tags: [pr, frontend, admin, jornadas]
status: merged
---

# PR #26 — feat(admin): gerenciar jornadas e etapas

## 🎯 Contexto

Ordem 24 de [[2026-09-28-plano-da-v1-do-frontend]]. Fecha a funcionalidade 6 de
[[visao-de-produto]].

## 🔧 Mudanças

- `src/paginas/admin/AdminJornadas.tsx`, `EditorJornada.tsx`, `Interruptor.tsx` (extraído).
- `src/dados/catalogo.ts` — `validarJornada`, `salvarJornada`, `alternarPublicacaoJornada`,
  `apagarJornada` (+ testes).
- `navegacao.tsx`, `App.tsx`.

## 🕵️ Dado pessoal (LGPD)

A lista mostra só **quantas** pessoas começaram cada jornada, nunca quem.

## 🧠 Decisões técnicas

- ⭐ **Id de etapa é estável**: etapa existente mantém o id ao editar/reordenar; só etapa nova ganha
  um. O progresso (`jornada/etapa`) sobrevive à edição — testado.
- Etapa nova recebe uma chave de React própria até ganhar id no salvamento — sem ela, reordenar
  remontaria os campos e perderia o foco.
- Conteúdo de apoio pode ser rascunho (marcado "(rascunho)"): a etapa só mostra o link quando o conteúdo
  está publicado.

## 🧪 Como testar

Ver [[AdminJornadas]].

## 📎 Documentação afetada

- [[AdminJornadas]]
- [[JornadaDetalhe]]
- [[2026]] (changelog)
