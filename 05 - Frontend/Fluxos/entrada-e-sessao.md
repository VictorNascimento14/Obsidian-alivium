---
tipo: funcionalidade
camada: frontend
area: Autenticacao
rota: /entrar → /
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, fluxo, autenticacao]
---

# Fluxo — entrada e sessão

1. Pessoa abre qualquer rota logada sem sessão → `ExigeSessao` manda para `/entrar` guardando a rota.
2. Em [[Entrar]], `entrar(email, senha)` confere o hash e grava `sessaoId` no repositório.
3. O `SomenteVisitante` percebe a sessão e leva para a rota guardada (ou `/`).
4. "Sair" no cabeçalho → `sair()` → `/entrar` com aviso "Até logo".

A sessão vive no `localStorage` ([[CamadaDeDados]]) e sobrevive a recarregar a página; outra aba
acompanha pela sincronização do repositório.

**Conta nova:** [[Cadastro]] cria a conta e abre a sessão no mesmo passo; a partir daí segue do item 3.

## Histórico de mudanças

- [[2026-09-28-pr-009-sessao-e-entrar]] — fluxo criado.
- [[2026-09-28-pr-010-tela-cadastro]] — entrada pelo cadastro.
