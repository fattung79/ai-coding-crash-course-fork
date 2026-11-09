# Directory Structure

```
app/
  routes.ts          Route table (config-based routing)
  root.tsx           Root layout, error boundary
  routes/            Route modules — loaders, actions, components
  services/          Data access layer, one module per domain concept
  components/        Shared components; components/ui is shadcn
  lib/               Cross-cutting helpers (session, access, validation, ppp, markdown)
  db/                Drizzle schema and connection
  test/setup.ts      In-memory test database helpers
drizzle/             Generated SQL migrations and snapshots
scripts/seed.ts      Seed data
request-logger/      Standalone model-request logging proxy
.agents/skills/      Repo skills (.claude/skills symlinks here)
```
