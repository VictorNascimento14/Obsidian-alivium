---
tipo: funcionalidade
camada: frontend
area: Conteudos
rota: /conteudos/:id
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, conteudos, progresso]
---

# Leitura

## O que é

A página de um conteúdo, aberta a partir da [[Biblioteca]].

## Onde está no código

`src/paginas/conteudos/Leitura.tsx`; progresso em `src/dados/progresso.ts`; [[AvisoApoio]].

## Comportamento

- Só conteúdo publicado; id inexistente mostra mensagem com link de volta.
- "Marcar como concluído" ↔ "Concluído" (desfaz com novo toque).
- Relacionados: até 3 da mesma categoria.

## Movimento e micro-interações

Barra de leitura no `toolbar` (gruda com o cabeçalho); ícone de concluído com `animate-pop`; data com
`fade-in`; relacionados com `rise` escalonado.

## Histórico de mudanças

- [[2026-09-28-pr-014-leitura]] — criada.
- [[2026-09-28-pr-015-salvos]] — botão de coração (salvar).
- [[2026-09-28-pr-025-admin-conteudos]] — corpo passa a usar [[CorpoDoConteudo]].
- [[2026-09-28-pr-028-guia-respiracao]] — [[GuiaDeRespiracao]] nos conteúdos de respiração.
