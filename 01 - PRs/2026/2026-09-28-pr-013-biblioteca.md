---
tipo: pr
data: 2026-09-28
autor: VictorNascimento14
projeto: Alivium
pr: 13
url: https://github.com/VictorNascimento14/Alivium/pull/13
branch: feat/biblioteca
tags: [pr, frontend, conteudos]
status: aberto
---

# PR #13 — feat(conteudos): biblioteca por categoria com busca e filtro por tipo

## 🎯 Contexto

Ordem 13 de [[2026-09-28-plano-da-v1-do-frontend]]. Funcionalidade 3 de [[visao-de-produto]].

## 🔧 Mudanças

- `src/paginas/conteudos/Biblioteca.tsx` — página.
- `src/componentes/ConteudoCard.tsx`, `tons.ts`, `texto.ts` (`paraBusca`).
- `src/navegacao.tsx` — item Conteúdos; `src/App.tsx` — rota.

## 🕵️ Dado pessoal (LGPD)

Só leitura do progresso (selo de concluído). Busca não é gravada.

## 🧠 Decisões técnicas

- Filtros em `useSearchParams` com `replace` — não enchem o histórico a cada tecla.
- Pílulas de categoria no `toolbar` do `PageShell`: grudam junto com o cabeçalho (invariante do kit).
- `outline-none` no input/select dentro da pílula **só** com `focus-within:ring` na pílula — senão o
  foco de teclado some.
- Lavanda e céu não existem nas rampas do kit; usam a paleta padrão do Tailwind com `dark:` explícito.

## ⚠️ Armadilhas e aprendizados

- Screenshot `fullPage` do Chrome headless desenha a coluna sem os rótulos (redimensiona a janela e o
  recorte `clip-path` do marcador se perde). Na tela real está certo; conferir sempre com screenshot da
  viewport.

## 🧪 Como testar

Ver [[Biblioteca]].

## 📎 Documentação afetada

- [[Biblioteca]]
- [[ConteudoCard]]
- [[Casca]]
- [[2026]] (changelog)
