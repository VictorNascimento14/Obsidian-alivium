---
tipo: indice
ultima_atualizacao: 2026-09-28
tags: [indice, produto]
---

# Visão de produto — Alivium (Alívio da Dor)

## O que é

Aplicação voltada para **adultos**, com proposta de **acolhimento, reflexão, cuidado e esperança**.
Funciona em **celular, tablet e computador**, com interface simples, agradável e fácil de usar.

## Funcionalidades gerais (escopo pedido pelo dono)

| # | Funcionalidade | Onde vive no app |
|---|---|---|
| 1 | Cadastro e login de usuários | `/entrar`, `/cadastro` |
| 2 | Área inicial personalizada | `/` (Início) |
| 3 | Conteúdos organizados por categorias | `/conteudos`, `/conteudos/:id` |
| 4 | Jornadas e experiências de acompanhamento | `/jornadas`, `/jornadas/:id` |
| 5 | Registro do progresso do usuário | `/progresso`, `/diario`, check-in de humor |
| 6 | Área administrativa de conteúdos | `/admin/*` |
| 7 | Possibilidade de ampliar no futuro | camada de dados isolada — [[ADR-001-frontend-primeiro-com-dados-locais]] |

## Tom

Acolhedor, sem pressa, sem culpa. Nada de "você falhou na sequência": o progresso é celebrado, a
ausência não é punida. Linguagem em segunda pessoa, frases curtas.

## Limite do produto

O Alivium **não substitui** atendimento psicológico, médico ou de emergência. Telas de conteúdo e o
diário mantêm visível o caminho para ajuda: **CVV — 188** (ligação gratuita, 24h) e **SAMU — 192**.

## Estado

Só front-end, com dados locais no navegador. Ver [[roadmap]].
