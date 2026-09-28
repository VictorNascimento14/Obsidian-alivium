---
tipo: pendencia
data: 2026-09-28
status: resolvida
tags: [pendencia, design]
---

# `Calendar` do kit capitaliza cada palavra

O cabeçalho do mês aparece como "Setembro De 2026". Visto em [[Progresso]] ([[2026-09-28-pr-020-progresso]]).

Correção provável: trocar `capitalize` por `first-letter:uppercase` no `Calendar` (mesma armadilha
resolvida no [[Diario]]). Vive em `src/ui/base/`, então precisa ser levada também ao kit
vidro-orgânico.

Resolvida em [[2026-09-28-pr-021-calendario-mes]].
