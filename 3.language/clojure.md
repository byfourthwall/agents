## Project Context

### Stack

- Clojure project managed by Emeralds (`em` CLI) on top of the Clojure CLI.
- `deps.edn` is the source of truth for dependencies.
- `em.json` wraps it and delegates to `clojure`.
- Compiler config comes from `em.json`.
- Emeralds documentation: https://github.com/Oblivious-Oblivious/Emeralds

### Testing

- Framework: `clojure.test` (built-in).
- Spec files live in `spec/` and end in `_spec.clj`.
- Spec namespaces end in `-spec`.
- Run with `em test` (uses `clojure -M:test`).

### Code Style

- Run `em lint` to format with `cljfmt` and analyze with `clj-kondo`.
- Prefer the standard library over adding dependencies.
- 2-space indent, final newline, LF, trimmed trailing whitespace.
- Max 80 chars/line. Follow existing script style.
- `kebab-case` namespaces and functions; file paths use underscores
  where namespaces use dashes.
