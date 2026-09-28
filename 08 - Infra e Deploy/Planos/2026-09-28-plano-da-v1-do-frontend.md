---
tipo: plano
data: 2026-09-28
status: em-andamento
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
