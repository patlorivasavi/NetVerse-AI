# NetVerse AI

An interactive AI ecosystem for exploring classical algorithms through explainable visual experiments.

## Run & Operate

- `pnpm --filter @workspace/api-server run dev` — run the API server (port 5000)
- `pnpm --filter @workspace/netverse-ai run dev` — run the NetVerse AI web app
- `pnpm run typecheck` — full typecheck across all packages
- `pnpm run build` — typecheck + build all packages
- `pnpm --filter @workspace/api-spec run codegen` — regenerate API hooks and Zod schemas from the OpenAPI spec
- `pnpm --filter @workspace/db run push` — push DB schema changes (dev only)
- Required env: `DATABASE_URL` — Postgres connection string

## Stack

- pnpm workspaces, Node.js 24, TypeScript 5.9
- Frontend: React, Vite, Tailwind CSS, Framer Motion, Lucide React
- API: Express 5
- DB: PostgreSQL + Drizzle ORM
- Validation: Zod (`zod/v4`), `drizzle-zod`
- API codegen: Orval (from OpenAPI spec)
- Build: esbuild (CJS bundle)

## Where things live

- `artifacts/netverse-ai/src/App.tsx` — routed NetVerse AI experience and local AI demonstrations
- `artifacts/netverse-ai/src/index.css` — dark observatory visual system and responsive styling
- `artifacts/netverse-ai` — deployable frontend artifact
- `artifacts/api-server` — shared API server scaffold, currently unused by the local-first frontend

## Architecture decisions

- Keep the first release frontend-only so algorithm runs remain local, fast, deterministic, and easy to explain during a PBL viva.
- Use a single routed SPA with feature views for the six intelligence modules plus lab, learning, and project context.
- Keep the algorithm visualizations intentionally small and observable instead of hiding execution behind black-box services.

## Product

NetVerse AI presents Pathfinder, GameMind, ConstraintX, LogicVault, PlanForge, and Probabilix as an interactive observatory. Users can run pathfinding, play against Minimax or Alpha-Beta Tic-Tac-Toe, animate N-Queens backtracking, derive facts through chaining, build state-space plans, calculate Bayes posteriors, compare modules in AI Lab, and learn the syllabus concepts behind them.

## User preferences

- The user wants a professional, unique, creative, polished glass UI with restrained animation and a premium AI research/product feel.

## Gotchas

- The web workflow supplies `PORT` and `BASE_PATH`; use the managed workflow or pass both variables for manual Vite builds.
- The API and mockup workflows are separate from the NetVerse AI frontend and are not required for the current local-first experience.

## Pointers

- See the `pnpm-workspace` skill for workspace structure, TypeScript setup, and package details
