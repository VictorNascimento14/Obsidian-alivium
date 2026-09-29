---
tipo: funcionalidade
camada: frontend
area: Shell
rota: —
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, shell, autenticacao]
---

# Guardas de sessão

## O que é

Componentes de rota que decidem quem entra onde. Moram em `src/sessao/`, nunca no componente da tela.

## Onde está no código

| Guarda | Regra |
|---|---|
| `ExigeSessao` | sem sessão → `/entrar`, com `state.de` = rota pedida |
| `SomenteVisitante` | com sessão → `state.de` ou `/` |
| `RotaAdmin` | rota de layout: sem papel `admin` → `/`; repassa o contexto do `Outlet` |
| `LayoutLogado` | não é guarda: monta a coluna com a conta da sessão e o "Sair" |

`useSessao()` devolve o `Usuario` da sessão ou `null`.

## Histórico de mudanças

- [[2026-09-28-pr-009-sessao-e-entrar]] — guardas criadas.
- [[2026-09-28-pr-023-admin-painel]] — `RotaAdmin`; grupos da coluna por papel.
