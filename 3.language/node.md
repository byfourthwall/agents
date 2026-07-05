## Project Context

### Stack

- Node.js TypeScript project managed by Emeralds (`em` CLI) on top of pnpm.
- `package.json` is the source of truth for dependencies.
- `em.json` wraps it and delegates to `pnpm`/`node`.
- Node runs `.ts` sources directly via type stripping; no build step.
- Compiler config comes from `em.json`.
- Emeralds documentation: https://github.com/Oblivious-Oblivious/Emeralds

### Testing

- Framework: `vitest`.
- Spec files live in `spec/` and end in `.spec.ts`.
- Run with `em test` (uses `vitest run`).

### Code Style

- Run `em lint` to format and lint sources using Prettier, ESLint,
  and `tsc --noEmit`.
- Prefer the standard library over adding dependencies.
- 2-space indent, final newline, LF, trimmed trailing whitespace.
- Max 80 chars/line. Follow existing script style.
- ES modules only; import with explicit `.ts` extensions.
- Only erasable TypeScript syntax (no enums or namespaces);
  `erasableSyntaxOnly` is enforced.
- Double quotes; `camelCase` functions and variables;
  `PascalCase` classes and types.
- Add focused tests for real behavior changes when practical.
