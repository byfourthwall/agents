## Project Context

### Stack

- Elixir project managed by Emeralds (`em` CLI) on top of Mix.
- `mix.exs` is the source of truth for dependencies.
- `em.json` wraps it and delegates to `mix`/`elixir`.
- Compiler config comes from `em.json`.
- Emeralds documentation: https://github.com/Oblivious-Oblivious/Emeralds

### Testing

- Framework: ExUnit.
- Spec files live in `spec/` and end in `_spec.exs`.
- Run with `em test` (uses `mix test`).
- Spec entry point is `spec/test_helper.exs`.

### Code Style

- Run `em lint` to format with `mix format` and analyze with `credo`.
- Prefer the standard library over adding dependencies.
- 2-space indent, final newline, LF, trimmed trailing whitespace.
- Max 80 chars/line. Follow existing script style.
- Add focused tests for real behavior changes when practical.
