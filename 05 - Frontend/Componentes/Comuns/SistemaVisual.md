---
tipo: funcionalidade
camada: frontend
area: Comuns
rota: —
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, design]
---

# Sistema visual (fundação)

## O que é

A camada `src/ui/` do kit vidro-orgânico. Decisão: [[ADR-002-sistema-visual-vidro-organico]].
Vocabulário de movimento: [[linguagem-visual]].

## Onde está no código

| Camada | Arquivo | Alcance |
|---|---|---|
| Rampas, vidro, animações | `src/ui/index.css` | app inteiro |
| Tokens do Tailwind | `tailwind.config.ts` | app inteiro |
| Movimento em JS | `src/ui/lib/motion.ts` (`stagger`, `usePrefersReducedMotion`) | quem anima em JS |
| Tema | `src/ui/lib/tema.ts` + script no `index.html` | app inteiro |
| Marca | `src/ui/lib/marca.ts` | logotipo, prefixo do storage |

## Comportamento

- Tema: claro / escuro / sistema, na classe `.dark` do `<html>`, aplicada antes da primeira pintura.
- Tudo o que anima se anula sob `prefers-reduced-motion`.

## Histórico de mudanças

- [[2026-09-28-pr-002-fundacao-visual]] — fundação instalada, marca Alivium.
