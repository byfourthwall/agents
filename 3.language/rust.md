## Project Context

### Stack

- Rust project managed by Emeralds (`em` CLI) on top of Cargo.
- `Cargo.toml` is the source of truth for targets and dependencies.
- `em.json` wraps it and delegates to `cargo`.
- Compiler config comes from `em.json`.
- Emeralds documentation: https://github.com/Oblivious-Oblivious/Emeralds

### Testing

- Framework: Rust's built-in `#[test]` attribute and `assert!` macros.
- Spec files live in `spec/` and end in `.spec.rs`.
- Spec files reach crate modules via `#[path = "../src/..."]`.
- Run with `em test` (uses `cargo test`).

### Code Style

- Run `em lint` to format sources using `cargo fmt`.
- Prefer the standard library over adding dependencies.
- 4-space indent (Rust convention), final newline, LF, trimmed
  trailing whitespace.
- Max 80 chars/line. Follow existing script style.
- Add focused tests for real behavior changes when practical.
