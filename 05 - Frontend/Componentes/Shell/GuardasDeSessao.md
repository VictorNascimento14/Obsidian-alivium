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
| `LayoutLogado` | não é guarda: monta a coluna com a conta da sessão e o "Sair" |

`useSessao()` devolve o `Usuario` da sessão ou `null`.

## Histórico de mudanças

- [[2026-09-28-pr-009-sessao-e-entrar]] — guardas criadas.
