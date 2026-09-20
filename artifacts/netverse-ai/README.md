# NetVerse AI

NetVerse AI is an interactive AI learning platform for exploring classical
search, reasoning, planning, constraint solving, adversarial decision-making,
and probability.

> Where Algorithms Think, Reason, Plan & Decide.

## What is included

- **Pathfinder** — animated BFS, DFS, UCS, Greedy Best-First, and A* search
- **GameMind** — Tic-Tac-Toe with Minimax and Alpha-Beta pruning
- **ConstraintX** — animated N-Queens backtracking and a compact timetable demo
- **LogicVault** — structured facts, rules, queries, and chaining traces
- **PlanForge** — state-space planning with an animated action sequence
- **Probabilix** — interactive Bayesian probability calculator
- **AI Lab** — comparison view for the six AI problem families
- **Learn** — syllabus-mapped field notes
- **About** — academic project context and editable team placeholders

The demonstrations run locally in the browser. There are no required API keys,
external AI services, or database dependencies.

## Run locally

This project is part of the Replit pnpm workspace. From the workspace root:

```bash
pnpm install
pnpm --filter @workspace/netverse-ai run dev
```

For a direct Vite build, provide the same environment variables used by the
managed workflow:

```bash
PORT=5173 BASE_PATH=/ pnpm --filter @workspace/netverse-ai run build
```

## Stack

- React
- TypeScript
- Vite
- Tailwind CSS
- Framer Motion
- Lucide React

## Project structure

```text
src/
  App.tsx       # Routed app, UI, and local algorithm demonstrations
  index.css     # Theme, glass interface, responsive styling
  main.tsx      # React entry point
```

## Academic purpose

NetVerse AI was created as a B.Tech Computer Science Artificial Intelligence
project to make classical AI concepts observable and explainable through
interactive visual execution.