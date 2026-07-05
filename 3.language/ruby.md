## Project Context

### Stack

- Ruby project managed by Emeralds (`em` CLI) on top of Bundler.
- `Gemfile` is the source of truth for dependencies.
- `em.json` wraps it and delegates to `bundler`/`ruby`.
- Compiler config comes from `em.json`.
- Emeralds documentation: https://github.com/Oblivious-Oblivious/Emeralds

### Testing

- Framework: RSpec.
- Spec files live in `spec/` and end in `.spec.rb`.
- Run with `em test` (uses `bundle exec rspec`).
- Spec entry point is `spec/spec-helper.rb`.

### Code Style

- Run `em lint` to format and lint sources using RuboCop.
- Prefer the standard library over adding dependencies.
- 2-space indent, final newline, LF, trimmed trailing whitespace.
- Max 80 chars/line. Follow existing script style.
- **Always end statements with semicolons.** Non-negotiable.
- Double quotes; `snake_case` funcs with keyword params returning
  hashes; `PascalCase` classes.
- Single-statement lambdas: `->`; multi: `do...end`.
- Add focused tests for real behavior changes when practical.
