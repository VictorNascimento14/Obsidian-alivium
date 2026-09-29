---
tipo: indice
ultima_atualizacao: 2026-09-28
tags: [indice, frontend]
camada: frontend
---

# Front-end — mapa

Stack: React 19 · Vite · TypeScript · Tailwind 3.4 · react-router-dom 7 · sistema visual
vidro-orgânico ([[ADR-002-sistema-visual-vidro-organico]]).

## Páginas
- [[Entrar]] — `/entrar`
- [[Cadastro]] — `/cadastro`
- [[Inicio]] — `/`
- [[Biblioteca]] — `/conteudos`
- [[Leitura]] — `/conteudos/:id`
- [[Salvos]] — `/salvos`
- [[Jornadas]] — `/jornadas`
- [[JornadaDetalhe]] — `/jornadas/:id`
- [[Diario]] — `/diario`
- [[Progresso]] — `/progresso`
- [[Perfil]] — `/perfil`
- [[PainelAdmin]] — `/admin`

## Componentes
- [[SistemaVisual]] — fundação do vidro-orgânico (`src/ui/`)
- [[Primitivos]] — blocos de interface (`src/ui/base/`)
- [[Casca]] — coluna, cabeçalho e barra do celular (`src/ui/shell/`, `src/navegacao.tsx`)
- [[GuardasDeSessao]] — `ExigeSessao`, `SomenteVisitante`, `LayoutLogado`
- [[CheckInCard]] — check-in de humor e dor
- [[ConteudoCard]] — cartão de conteúdo
- [[AvisoApoio]] — CVV 188 / SAMU 192
- [[JornadaCard]] — cartão de jornada

## Fluxos
- [[entrada-e-sessao]] — do `/entrar` ao Início

## Camada de dados
- [[CamadaDeDados]] — tipos, sementes e repositório local (`src/dados/`)
