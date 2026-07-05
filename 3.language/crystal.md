## Project Context

### Stack

- Crystal project managed by Emeralds (`em` CLI) on top of Shards.
- `shard.yml` is the source of truth for targets and dependencies.
- `em.json` wraps it and delegates to `shards`/`crystal`.
- Compiler config comes from `em.json`.
- Emeralds documentation: https://github.com/Oblivious-Oblivious/Emeralds

### Testing

- Framework: Crystal's built-in `spec`.
- Spec files live in `spec/` and end in `.spec.cr`.
- Run with `em test` (uses `crystal spec`).

### Code Style

- Avoid manual types AT ALL COSTS.  Only type when necessary, let
  type inference do the work.
- Run `em lint` to format and lint documents using ameba.
- Prefer the standard library over adding dependencies.
- Keep Crystal code style local: 2-space indent, final newline, LF,
  trimmed trailing whitespace.
- When creating/extending classes, private methods are first, then
  initialize method, then protected, then public.
- Max 80 chars/line. Follow existing script style.
- Crystal statements end with semicolons. Match surrounding files.
- Add focused tests for real behavior changes when practical.
- Single-statement lambdas: `->`; multi: `do...end`.

### Performance

- Follow the guidelines in the Crystal Performance Guide.
- Source: https://crystal-lang.org/reference/1.20/guides/performance.html

### Concurrency

- Follow the guidelines in the Crystal Concurrency Guide.
- Source: https://crystal-lang.org/reference/1.20/guides/concurrency.html
