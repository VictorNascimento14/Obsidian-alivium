---
tipo: funcionalidade
camada: frontend
area: Autenticacao
rota: /cadastro
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, autenticacao]
---

# Cadastro

## O que é

Criação de conta com papel `pessoa`. Mesma moldura de [[Entrar]].

## Onde está no código

`src/paginas/autenticacao/Cadastro.tsx`; regras em `src/dados/usuarios.ts` (`validarCadastro`,
`cadastrar`, `forcaDaSenha`).

## Comportamento

| Campo | Regra |
|---|---|
| Nome | 2 a 80 caracteres |
| E-mail | formato válido, único (normalizado) |
| Senha | mínimo 8; força 1–4 é só orientação |
| Aviso | obrigatório marcar |

Sucesso: conta criada, sessão aberta, Início com aviso "Boas-vindas".

## Movimento e micro-interações

Barra de força com `transition-all duration-open ease-organic`; erros com `fade-up`; link com
`.underline-grow`.

## Histórico de mudanças

- [[2026-09-28-pr-010-tela-cadastro]] — tela criada.
