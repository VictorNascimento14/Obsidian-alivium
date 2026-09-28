---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 10
url: https://github.com/VictorNascimento14/Alivium/pull/10
branch: feat/tela-cadastro
tags: [pr, frontend, autenticacao]
status: merged
---

# PR #10 — feat(autenticacao): tela de cadastro com validação e força da senha

## 🎯 Contexto

Ordem 10 de [[2026-09-28-plano-da-v1-do-frontend]]. Completa a funcionalidade 1 de
[[visao-de-produto]], com [[Entrar]].

## 🔧 Mudanças

- `src/paginas/autenticacao/Cadastro.tsx` — tela.
- `src/dados/usuarios.ts` — `validarCadastro`, `cadastrar`, `forcaDaSenha`, `SENHA_MINIMA` (+ testes).
- `Entrar.tsx` ganha o link para o cadastro; `App.tsx` ganha a rota.

## 🕵️ Dado pessoal (LGPD)

Nome, e-mail e hash da senha passam a ser gravados no `localStorage`. O consentimento na tela diz isso
em linguagem simples antes do primeiro dado ser gravado.

## 🧠 Decisões técnicas

- Validação em `src/dados/` (regra) e reaproveitada pela tela (conforto) — a mesma função, sem duas
  versões da regra.
- Força da senha orienta, não bloqueia; o bloqueio é só o tamanho mínimo (8).
- Barra de força com classes literais por nível (`w-1/4`…`w-full`) — classe montada em runtime não
  existe no build.

## ⚠️ Armadilhas e aprendizados

- Os ícones dos campos ficaram **escondidos atrás do próprio campo**: bug do `TextField` do kit,
  corrigido no PR seguinte.

## 🧪 Como testar

Ver [[Cadastro]].

## 📎 Documentação afetada

- [[Cadastro]]
- [[entrada-e-sessao]]
- [[2026]] (changelog)
