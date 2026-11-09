# Conventions

- Service and lib modules open with a `// ─── Name ───` comment header summarising the module's responsibility; several also record the reasoning behind non-obvious decisions. Read those headers before changing a module.
- Enums are TypeScript `enum`s exported from `app/db/schema.ts` and used at every insert site, including `scripts/seed.ts`.
- Server-only modules use the `.server.ts` suffix.
- `data.db` is disposable and gitignored; `scripts/seed.ts` is the source of truth for starting data.
