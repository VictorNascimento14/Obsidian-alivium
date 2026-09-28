---
tipo: aprendizado
data: 2026-09-28
contexto: PR #19
tags: [aprendizado, acessibilidade, react]
---

# Foco no botão de sugestão: cada espaço "clica" de novo

## O sintoma

No teste de ponta a ponta do [[Diario]], tocar em "Hoje eu senti…" e digitar em seguida resultou em
"Hoje eu senti…" repetido sete vezes — e nada do que foi digitado.

## A causa

O foco ficou no `<button>` da sugestão. Espaço (e Enter) num botão focado dispara clique: cada espaço
da frase inseria a sugestão de novo. Na segunda tentativa, com o foco movido num
`requestAnimationFrame`, o cursor era reposicionado **depois** das primeiras teclas, embaralhando o
texto.

## A correção

`flushSync` aplica o texto novo, e no mesmo clique o foco vai para o campo com o cursor no fim
([[2026-09-28-pr-019-diario]]).

## Como evitar

Botão que insere algo num campo devolve o foco a esse campo **de forma síncrona**. Adiar para o próximo
quadro deixa uma janela em que o teclado ainda age sobre o botão.
