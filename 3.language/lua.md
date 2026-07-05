## Project Context

### Stack

- Lua project managed by Emeralds (`em` CLI) on top of LuaRocks.
- `em.json` is the source of truth for dependencies.
- `em install` resolves entries in `em.json` via `luarocks`.
- Compiler config comes from `em.json`.
- Emeralds documentation: https://github.com/Oblivious-Oblivious/Emeralds

### Testing

- Framework: busted.
- Spec files live in `spec/` and end in `.spec.lua`.
- Run with `em test` (uses `busted`).
- Spec entry point is `spec/spec-helper.lua`.

### Code Style

- Run `em lint` to lint sources using selene.
- Prefer the standard library over adding dependencies.
- 2-space indent, final newline, LF, trimmed trailing whitespace.
- Max 80 chars/line. Follow existing script style.
- Modules return a table (`local M = {}; ... return M;`).
- Add focused tests for real behavior changes when practical.
