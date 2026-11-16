# Orviaflow

A personal operating system for managing daily life, built as a web app and PWA.

## Modules (planned)

- **Finance:** bank accounts, savings, expenses, targets, subscriptions, and debts/credits
- **Work:** task backlog, projects with custom statuses and tags, a calendar, and a daily kanban
- **Task ↔ finance links:** a task's budget appears in upcoming expenses; its expected income appears in incoming income
- **Notes and whiteboard:** rich notes with images and a whiteboard for each project
- **AI assistant:** performs actions in the app and builds custom dashboard widgets from exposed data variables

## Structure

```
apps/
  web/   React + TypeScript (Vite)
  api/   NestJS + TypeScript
packages/  shared code (planned)
```

## Requirements

- Node 24+
- pnpm (`corepack enable`)

## Getting started

```bash
pnpm install
pnpm dev       # web + api together
pnpm dev:web   # http://localhost:5173
pnpm dev:api   # http://localhost:3000
```

## Scripts

| Command             | Description                      |
| ------------------- | -------------------------------- |
| `pnpm lint`         | Lint all apps with ESLint        |
| `pnpm lint:fix`     | Lint and auto-fix                |
| `pnpm format`       | Format all files with Prettier   |
| `pnpm format:check` | Check formatting without writing |
| `pnpm typecheck`    | Type-check every app             |

## Conventions

- Commit messages follow [Conventional Commits](https://www.conventionalcommits.org/), e.g. `feat: add accounts page`. This is enforced by commitlint.
- A pre-commit hook runs ESLint and Prettier on staged files.
