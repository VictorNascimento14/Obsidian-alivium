---
tipo: funcionalidade
camada: frontend
area: Comuns
rota: —
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, dados]
---

# Camada de dados (`src/dados/`)

## O que é

A fronteira entre as telas e a persistência. Decisão: [[ADR-001-frontend-primeiro-com-dados-locais]].

## Onde está no código

| Arquivo | Papel |
|---|---|
| `src/dados/tipos.ts` | domínio: usuário, categoria, conteúdo, jornada, etapa, check-in, diário, progresso |
| `src/dados/sementes.ts` | estado de um navegador novo; contas de demonstração |

## Comportamento

- Contas de demonstração (senha `alivium123`): `admin@alivium.app` (papel `admin`) e
  `pessoa@exemplo.com` (papel `pessoa`).
- Datas de calendário `AAAA-MM-DD` local; instantes em ISO completo.

## Histórico de mudanças

- [[2026-09-28-pr-007-dominio-e-sementes]] — tipos do domínio e sementes.
