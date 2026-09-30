---
tipo: pendencia
data: 2026-09-28
status: resolvida
tags: [pendencia, design]
---

# Levar duas correções ao kit vidro-orgânico

O Alivium corrigiu dois defeitos em `src/ui/base/` que existem igual no kit de origem
(`VictorNascimento14/Design-moderno`). A relação é de cópia, não de dependência — a correção só chega
lá se alguém a levar ([[ADR-002-sistema-visual-vidro-organico]]).

| Defeito | Correção aqui |
|---|---|
| Ícone do `TextField` escondido atrás do campo | [[2026-09-28-pr-011-icone-do-campo]] |
| `Calendar` com "Setembro De 2026" | [[2026-09-28-pr-021-calendario-mes]] |

Decisão do dono: abrir PR no kit, ou não. Nada foi alterado lá.

## Resolução (2026-09-30)

As duas correções entraram no kit por PR, com issue:

| Defeito | No kit |
|---|---|
| Ícone do `TextField` | [Design-moderno#3](https://github.com/VictorNascimento14/Design-moderno/pull/3) (issue #1) |
| Rótulo do `Calendar` | [Design-moderno#4](https://github.com/VictorNascimento14/Design-moderno/pull/4) (issue #2) |

Projeto novo instalado a partir de agora já recebe as duas corrigidas.
