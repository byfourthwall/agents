## Project Context

### Stack

- Zig project managed by Emeralds (`em` CLI).
- `build.zig.zon` is the source of truth for dependencies.
- `build.zig` defines targets and steps.
- `em.json` wraps them and delegates to `zig`.
- Compiler config comes from `em.json`.
- Emeralds documentation: https://github.com/Oblivious-Oblivious/Emeralds

### Testing

- Framework: Zig's built-in `test` blocks and `std.testing`.
- Spec files live in `spec/` and end in `.spec.zig`.
- `spec/<name>.spec.zig` aggregates all spec files via
  `comptime { _ = @import(...); }`.
- Run with `em test` (uses `zig build test`).

### Code Style

- Run `em lint` to format sources using `zig fmt`.
- Prefer the standard library over adding dependencies.
- 4-space indent (Zig convention), final newline, LF, trimmed
  trailing whitespace.
- `src/<name>.libs.zig` re-exports modules; spec tests reach them
  via `@import("__libs__")`.
- Add focused tests for real behavior changes when practical.
