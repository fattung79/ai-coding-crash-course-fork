# Development Commands

`README.md` holds first-time setup, the standard npm scripts (`dev`, `build`, `test`, `typecheck`, `db:migrate`, `db:seed`, `reset`, `cherry-pick`), the course's section structure, and lesson-checkpoint navigation — read it when you need any of those. Scripts it omits:

| Command                  | What it does                                                    |
| ------------------------ | --------------------------------------------------------------- |
| `npm start`              | Serve the production build                                      |
| `npm run db:generate`    | Generate a Drizzle migration from `app/db/schema.ts`            |
| `npm run pull`           | Pull upstream `main` updates into the working branch            |
| `npm run request-logger` | Proxy that logs every request a coding agent sends to the model |
| `npm run loc`            | Line count across tracked source files                          |

`npm run db:seed` drops, migrates, and reseeds the database from `scripts/seed.ts`.

Run a single test file:

```bash
npx vitest run app/services/courseService.test.ts
```

Run a single test by name:

```bash
npx vitest run app/services/courseService.test.ts -t "returns published courses"
```

`npm run typecheck` runs `react-router typegen` first, which regenerates the per-route type modules under `.react-router/types`. Running `tsc` on its own will report missing `./+types/*` imports.

Formatting is Prettier, configured in `.prettierrc` (2 spaces, double quotes, semicolons, 80 columns, ES5 trailing commas). There is no ESLint setup and no lint script.
