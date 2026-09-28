---
tipo: funcionalidade
camada: frontend
area: Perfil
rota: /perfil
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, perfil, lgpd]
---

# Perfil

## O que é

Dados da conta, aparência e controle dos próprios dados. Acesso pelo bloco da conta na coluna.

## Onde está no código

`src/paginas/perfil/Perfil.tsx`; regras em `src/dados/usuarios.ts`.

## Comportamento

| Ação | Regra |
|---|---|
| Nome | 2–80 caracteres |
| Intenção | até 120; vazia = some do Início |
| Tema | claro / escuro / sistema (`definirTema`) |
| Baixar dados | JSON sem hash da senha |
| Apagar conta | digitar "apagar"; cascata; última admin bloqueada |

## Movimento e micro-interações

Avatar com `pop`; cartões com `rise` escalonado; seletor de tema com a pílula ativa em
`bg-primary-900 shadow-nav-active`; modal do kit.

## Histórico de mudanças

- [[2026-09-28-pr-022-perfil]] — criada.
