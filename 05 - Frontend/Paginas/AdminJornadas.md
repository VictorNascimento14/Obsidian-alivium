---
tipo: funcionalidade
camada: frontend
area: Administracao
rota: /admin/jornadas · /admin/jornadas/:id
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, admin, jornadas]
---

# Administração — Jornadas

## O que é

Lista e editor das [[Jornadas]] e de suas etapas.

## Onde está no código

`src/paginas/admin/AdminJornadas.tsx`, `EditorJornada.tsx` (`nova` ou id); regras em
`src/dados/catalogo.ts`; [[SeletoresDoCatalogo]].

## Comportamento

| Regra | Valor |
|---|---|
| Título | 3–60 |
| Descrição | até 160 |
| Etapas | ≥ 1; título 2–60; proposta 5–200; conteúdo opcional e existente |
| Ids das etapas | preservados na edição (o progresso depende deles) |

## Movimento e micro-interações

Etapas entram com `fade-up`; botões de ordem com `.press` e desabilitados nas pontas; "Adicionar etapa"
tracejado que acende no hover; interruptor deslizante.

## Histórico de mudanças

- [[2026-09-28-pr-026-admin-jornadas]] — criada.
