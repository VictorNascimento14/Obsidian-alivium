---
tipo: funcionalidade
camada: frontend
area: Inicio
rota: /
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, inicio]
---

# Início

## O que é

A área inicial personalizada: o primeiro lugar depois de entrar.

## Onde está no código

`src/paginas/inicio/Inicio.tsx`, `frases.ts`; cartão [[CheckInCard]].

## Comportamento

- Saudação por horário (5h–12h bom dia · 12h–18h boa tarde · resto boa noite) + primeiro nome.
- Intenção pessoal da conta, ou texto de acolhimento.
- Frase para hoje: escolhida pelo dia do ano, estável durante o dia.
- Continue de onde parou: jornada em andamento iniciada mais recentemente ([[JornadaDetalhe]]).
- Para você hoje: 3 conteúdos não concluídos; dia difícil (humor ≤ 2 ou dor ≥ 7) põe práticas e respirações curtas primeiro.

## Movimento e micro-interações

Cartões com `rise` escalonado; halo decorativo no topo; cartão da frase com `.lift` + `.sheen`.

## Histórico de mudanças

- [[2026-09-28-pr-012-inicio-checkin]] — saudação, intenção, check-in e frase do dia.
- [[2026-09-28-pr-018-inicio-continuar]] — continuar jornada e recomendações.
