---
tipo: funcionalidade
camada: frontend
area: Administracao
rota: /admin
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, admin]
---

# Painel da administração

## O que é

A entrada da área administrativa, só para papel `admin` ([[GuardasDeSessao]]).

## Onde está no código

`src/paginas/admin/PainelAdmin.tsx`; `src/dados/admin.ts`.

## Comportamento

Indicadores (pessoas, conteúdos, rascunhos, jornadas, check-ins em 7 dias), ranking de conclusões e
humor médio da semana. Só agregados.

## Movimento e micro-interações

`StatCard` com `AnimatedNumber`; ranking com `MeterBar` escalonada; emoji do clima em `pop`.

## Histórico de mudanças

- [[2026-09-28-pr-023-admin-painel]] — criado.
