# deposit-slip-web

This directory is a scaffold for the deposit slip web workspace. It groups the web app, shared packages, renderer utilities, local infrastructure, and helper scripts.

## Structure
- `apps/web/src/app` – application routes and top-level React (or comparable) views.
- `apps/web/src/components` – shared UI components for the web experience.
- `apps/web/src/lib` – client-side utilities and hooks.
- `apps/web/src/server/{api,auth,db,jobs,storage}` – server-side endpoints, authentication handlers, database logic, background jobs, and storage integrations.
- `packages/shared/src/{schemas,types,units}` – reusable validation schemas, shared TypeScript types, and unit helpers.
- `packages/renderer/src/{layout,pagination,fonts,tests}` – rendering concerns for layout, pagination, font loading, and renderer-focused tests.
- `infra` – local development services with `docker-compose.yml` plus data directories for Postgres and Redis.
- `scripts` – helper scripts for running, testing, or maintenance workflows.

## Usage
- Fill the `.gitkeep` files with real implementations as features are added.
- Use `infra/docker-compose.yml` to spin up local Postgres and Redis instances during development.
- Export renderer modules through `packages/renderer/src/index.ts` as they become available.
