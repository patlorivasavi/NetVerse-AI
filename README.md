# NetVerse AI

NetVerse AI is an interactive AI experimentation platform for exploring
classical search, adversarial decision-making, constraint solving, symbolic
reasoning, planning, and probability.

The main web app lives in:

```text
artifacts/netverse-ai
```

## Run the web app

From the repository root:

```bash
pnpm install
pnpm --filter @workspace/netverse-ai run dev
```

The app includes:

- Pathfinder — BFS, DFS, UCS, Greedy Best-First, and A*
- GameMind — Minimax and Alpha-Beta Tic-Tac-Toe
- ConstraintX — N-Queens backtracking and timetable demo
- LogicVault — facts, rules, queries, and chaining traces
- PlanForge — state-space planning
- Probabilix — interactive Bayes calculator
- AI Lab — comparative view of the six modules
- Learn and About pages for the academic project

The demonstrations run locally in the browser and do not require external
AI APIs, API keys, or a database.

## Workspace layout

```text
artifacts/netverse-ai/   # NetVerse AI frontend
artifacts/api-server/    # Shared API server scaffold
lib/                     # Shared workspace libraries
scripts/                 # Workspace utilities
```

See `artifacts/netverse-ai/README.md` for the app-specific details.