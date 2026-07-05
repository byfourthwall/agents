## Project Context

### Stack

- C language project managed by Emeralds (`em` CLI).
- Compiler config comes from `em.json`.
- Emeralds documentation: https://github.com/Oblivious-Oblivious/Emeralds

### Testing

- Using cSpec framework: https://github.com/Oblivious-Oblivious/cSpec

### Code Style

- Favour C89 compatibility by default; only use newer C features when
  explicitly told to.
- `.clang-format` is authoritative. Don't override it.
- `.clangd` provides editor intelligence.
