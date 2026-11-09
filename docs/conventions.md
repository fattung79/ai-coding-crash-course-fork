# Conventions

- Open new service and lib modules with a `// ─── Name ───` comment header stating the module's responsibility and the reasoning behind any non-obvious decisions.
- Services take positional parameters, not options objects.
- Enums are TypeScript `enum`s exported from `app/db/schema.ts`.
- Server-only modules use the `.server.ts` suffix.
- Typecheck with `npm run typecheck`; bare `tsc` reports missing `./+types/*` imports.
- Format changed files with `npx prettier --write <files>`.
