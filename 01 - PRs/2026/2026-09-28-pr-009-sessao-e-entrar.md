---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 9
url: https://github.com/VictorNascimento14/Alivium/pull/9
branch: feat/sessao-e-entrar
tags: [pr, frontend, autenticacao]
status: merged
---

# PR #9 — feat(sessao): sessão local, guardas de rota e tela de entrar

## 🎯 Contexto

Ordem 8–9 de [[2026-09-28-plano-da-v1-do-frontend]]: sessão e login. Funcionalidade 1 de
[[visao-de-produto]].

## 🔧 Mudanças

- `src/dados/usuarios.ts` — `entrar`, `sair`, `hashSenha`, `normalizarEmail`.
- `src/dados/sha256.ts` (+ testes) — hash síncrono.
- `src/sessao/useSessao.ts`, `src/sessao/Guardas.tsx`, `src/sessao/LayoutLogado.tsx`.
- `src/paginas/autenticacao/{LayoutAutenticacao,Entrar,VerSenha}.tsx`.
- `src/App.tsx` — rotas sem sessão × com sessão; `src/navegacao.tsx` perde a conta fixa.

## 🕵️ Dado pessoal (LGPD)

E-mail e hash de senha ficam no `localStorage` deste navegador. A mensagem de erro é a mesma para
e-mail inexistente e senha errada — a tela não revela quem tem conta.

## 🧠 Decisões técnicas

- **SHA-256 em JS puro em vez de `crypto.subtle`**: `subtle` só existe em contexto seguro; abrir o app
  pelo IP da rede local no celular quebraria o login. Marcado com `ponytail:` no arquivo.
- **Quem redireciona depois do login é a guarda `SomenteVisitante`**, não a tela: evita duas
  navegações concorrentes quando a sessão aparece.
- `conta` e `onSair` memorizados no `LayoutLogado` — referência nova a cada render refaria o contexto
  de todas as telas.
- Sem "carregando" artificial no botão: a verificação é instantânea, e fingir espera seria desonesto.

## 🧪 Como testar

Ver [[Entrar]] e [[entrada-e-sessao]].

## 📎 Documentação afetada

- [[Entrar]]
- [[entrada-e-sessao]]
- [[GuardasDeSessao]]
- [[2026]] (changelog)
