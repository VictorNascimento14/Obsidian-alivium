---
tipo: funcionalidade
camada: frontend
area: Comuns
rota: —
ultima_atualizacao: 2026-09-28
tags: [funcionalidade, design]
---

# Primitivos do sistema visual

## O que é

Os blocos de interface de `src/ui/base/`, vindos do kit vidro-orgânico. Base: [[SistemaVisual]].

## Onde está no código

| Primitivo | Para quê |
|---|---|
| `GlassCard` | cartão de vidro (soft/medium/strong), entra subindo; `interactive` levanta, `sheen` brilha |
| `GlassPill` | cápsula do cabeçalho e dos filtros |
| `StatCard` | indicador com pastilha de ícone |
| `MeterBar` | barra que cresce ao entrar na tela |
| `AnimatedNumber` | conta de zero até o valor; par `sr-only` |
| `Button` | pílula em 4 variantes; `type="button"` por padrão |
| `TextField` | campo em pílula com ícone, dica, erro, sucesso |
| `Modal` | cortina + vidro forte em portal; Escape e clique fora fecham |
| `Dropdown` | painel que desdobra/dobra, montado quando fechado (`inert`) |
| `Glyph` | ícones próprios, traçado 2.5 — o Alivium acrescentou `home`, `book`, `compass`, `pen`, `heart`, `leaf` |
| `Avatar` | iniciais com cor derivada do nome |
| `Reveal` | entrada para o que não é cartão |
| `Calendar` | calendário mensal com dias marcados |

## Histórico de mudanças

- [[2026-09-28-pr-003-primitivos]] — primitivos instalados.
- [[2026-09-28-pr-004-icones]] — seis ícones de navegação no `Glyph`.
- [[2026-09-28-pr-011-icone-do-campo]] — ícone do `TextField` com `z-10` (não ficava visível).
