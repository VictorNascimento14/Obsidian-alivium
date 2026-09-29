---
tipo: funcionalidade
camada: frontend
area: Autenticacao
rota: /entrar
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, autenticacao]
---

# Entrar

## O que é

A porta de entrada do app. Fica fora da coluna ([[ADR-002-sistema-visual-vidro-organico]]).

## Onde está no código

`src/paginas/autenticacao/Entrar.tsx`, moldura em `LayoutAutenticacao.tsx`, olho em `VerSenha.tsx`.

## Comportamento

- E-mail normalizado (minúsculas, sem espaço). Erro único para "não existe" e "senha errada".
- Atalhos "Pessoa" e "Administração" preenchem as contas de demonstração.
- Depois de entrar, a guarda leva ao destino guardado ou ao Início ([[GuardasDeSessao]]).

## Movimento e micro-interações

Halos com `fade-in`; marca, título, texto e pílulas com `rise` escalonado (`stagger`); pílulas `.lift`;
cartão `rise`; erro com `fade-up`; atalhos `.press` + `.lift`.

## Histórico de mudanças

- [[2026-09-28-pr-009-sessao-e-entrar]] — tela criada.
- [[2026-09-28-pr-022-perfil]] — mostra só as demonstrações que ainda existem.
