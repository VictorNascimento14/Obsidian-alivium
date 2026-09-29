---
tipo: plano
data: 2026-09-28
status: resolvida
tags: [plano, frontend, v1]
---

# Plano da v1 do front-end

Um PR por funcionalidade, pequeno, mergeado por squash antes do próximo começar (evita PR empilhado
contra base morta).

| Ordem | Branch | Entrega |
|---|---|---|
| 1 | `chore/scaffolding` | Vite + React + TS + ESLint, página mínima |
| 2 | `ui/fundacao-visual` | `index.css`, Tailwind, tema, movimento |
| 3 | `ui/primitivos` | GlassCard, Button, TextField, Modal, Dropdown… |
| 4 | `ui/casca` | coluna lateral, cabeçalho, barra do celular, marca Alivium |
| 5 | `chore/ci` | CI de lint/type-check/build + checagem da seção de documentação |
| 6 | `feat/dominio-e-sementes` | tipos do domínio e conteúdo inicial |
| 7 | `feat/repositorio-local` | store com `localStorage` |
| 8 | `feat/sessao-e-rotas` | sessão, guarda de rota, navegação |
| 9 | `feat/tela-entrar` | login |
| 10 | `feat/tela-cadastro` | cadastro |
| 11 | `feat/inicio-checkin` | saudação personalizada + check-in de humor |
| 12 | `feat/inicio-continuar` | continuar jornada, recomendados |
| 13 | `feat/biblioteca` | conteúdos por categoria, busca |
| 14 | `feat/leitura` | leitura do conteúdo, concluir |
| 15 | `feat/salvos` | favoritos |
| 16 | `feat/jornadas-lista` | lista de jornadas |
| 17 | `feat/jornada-detalhe` | etapas da jornada |
| 18 | `feat/progresso` | painel de progresso |
| 19 | `feat/diario` | diário de reflexões |
| 20 | `feat/perfil` | perfil e preferências |
| 21 | `feat/admin-painel` | painel admin + guarda de papel |
| 22 | `feat/admin-categorias` | CRUD de categorias |
| 23 | `feat/admin-conteudos` | CRUD de conteúdos |
| 24 | `feat/admin-jornadas` | CRUD de jornadas e etapas |
| 25 | `feat/apoio-e-404` | aviso de apoio (CVV), página 404 |
| 26 | `chore/pwa-meta` | manifest, ícone, metadados |

A numeração dos PRs no GitHub pode não bater 1:1 com a ordem — a nota de cada PR é a fonte.

## Como terminou (2026-09-28)

Concluído em **30 PRs**, todos com squash e CI verde. A ordem real divergiu em pontos
(o "continuar" do Início veio depois das jornadas, que ele usa; entraram três correções e o guia de
respiração). Mapa real:

| PR | Nota | Título |
|---|---|---|
| #1 | [[2026-09-28-pr-001-scaffolding]] | chore: scaffolding Vite + React + TypeScript + ESLint |
| #2 | [[2026-09-28-pr-002-fundacao-visual]] | ui(fundacao): instalar a fundação do sistema vidro-orgânico |
| #3 | [[2026-09-28-pr-003-primitivos]] | ui(primitivos): instalar os primitivos do vidro-orgânico |
| #4 | [[2026-09-28-pr-004-icones]] | ui(icones): acrescentar ícones de navegação do Alivium ao Glyph |
| #5 | [[2026-09-28-pr-005-casca]] | ui(casca): instalar coluna lateral, cabeçalho e barra do celular |
| #6 | [[2026-09-28-pr-006-ci]] | chore(ci): rodar lint, type-check e build e exigir o link do cofre no PR |
| #7 | [[2026-09-28-pr-007-dominio-e-sementes]] | feat(dados): tipos do domínio e conteúdo inicial |
| #8 | [[2026-09-28-pr-008-repositorio-local]] | feat(dados): repositório local com persistência e testes |
| #9 | [[2026-09-28-pr-009-sessao-e-entrar]] | feat(sessao): sessão local, guardas de rota e tela de entrar |
| #10 | [[2026-09-28-pr-010-tela-cadastro]] | feat(autenticacao): tela de cadastro com validação e força da senha |
| #11 | [[2026-09-28-pr-011-icone-do-campo]] | fix(ui): ícone do TextField ficava escondido atrás do campo |
| #12 | [[2026-09-28-pr-012-inicio-checkin]] | feat(inicio): saudação personalizada e check-in de humor e dor |
| #13 | [[2026-09-28-pr-013-biblioteca]] | feat(conteudos): biblioteca por categoria com busca e filtro por tipo |
| #14 | [[2026-09-28-pr-014-leitura]] | feat(conteudos): leitura com progresso, conclusão e relacionados |
| #15 | [[2026-09-28-pr-015-salvos]] | feat(conteudos): salvar conteúdos e página de salvos |
| #16 | [[2026-09-28-pr-016-jornadas-lista]] | feat(jornadas): lista de jornadas com andamento |
| #17 | [[2026-09-28-pr-017-jornada-detalhe]] | feat(jornadas): detalhe da jornada com etapas e próximo passo |
| #18 | [[2026-09-28-pr-018-inicio-continuar]] | feat(inicio): continuar jornada e conteúdos recomendados para o dia |
| #19 | [[2026-09-28-pr-019-diario]] | feat(diario): diário de reflexões com sugestões, edição e exclusão |
| #20 | [[2026-09-28-pr-020-progresso]] | feat(progresso): painel com indicadores, humor e dias de cuidado |
| #21 | [[2026-09-28-pr-021-calendario-mes]] | fix(ui): mês do calendário com só a primeira letra maiúscula |
| #22 | [[2026-09-28-pr-022-perfil]] | feat(perfil): perfil, tema e controle dos próprios dados |
| #23 | [[2026-09-28-pr-023-admin-painel]] | feat(admin): painel administrativo com métricas agregadas e guarda de papel |
| #24 | [[2026-09-28-pr-024-admin-categorias]] | feat(admin): gerenciar categorias do catálogo |
| #25 | [[2026-09-28-pr-025-admin-conteudos]] | feat(admin): gerenciar conteúdos com editor e prévia ao vivo |
| #26 | [[2026-09-28-pr-026-admin-jornadas]] | feat(admin): gerenciar jornadas e etapas |
| #27 | [[2026-09-28-pr-027-404-e-erro]] | feat(sistema): página não encontrada e tela de erro acolhedoras |
| #28 | [[2026-09-28-pr-028-guia-respiracao]] | feat(conteudos): guia animado de respiração |
| #29 | [[2026-09-28-pr-029-icone-e-manifesto]] | chore(pwa): ícone, manifesto e metadados do app |
| #30 | [[2026-09-28-pr-030-readme]] | docs(readme): como rodar, contas de demonstração e mapa do app |
