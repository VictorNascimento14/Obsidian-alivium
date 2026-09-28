---
tipo: runbook
camada: infra
escopo: CI do repositório de código
ultima_atualizacao: 2026-09-28
tags: [runbook, infra, ci]
tempo_estimado: 5 min
---

# Runbook — CI vermelho

## Quando usar

Um PR no `Alivium` ficou vermelho.

## Passos

1. **"lint · type-check · build"** — rode local o mesmo que falhou: `npm run lint`,
   `npm run type-check` ou `npm run build`. Corrija e dê push na mesma branch.
2. **"seção 📓 Documentação"** — o corpo do PR não tem `## 📓 Documentação` com link para
   `VictorNascimento14/Obsidian-alivium`. Escreva a nota no cofre, edite o corpo do PR
   (`gh api repos/:owner/:repo/pulls/NNN -X PATCH -F body=@corpo.md`); o check roda de novo na edição.

## Como saber que deu certo

`gh pr checks NNN` mostra os dois verdes. Criado em [[2026-09-28-pr-006-ci]].
