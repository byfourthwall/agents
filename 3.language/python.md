## Project Context

### Stack

- Python project managed by Emeralds (`em` CLI) on top of uv.
- `em.json` is the source of truth for dependencies.
- `em install` adds em.json deps via `uv add`, then syncs.
- Compiler config comes from `em.json`.
- Emeralds documentation: https://github.com/Oblivious-Oblivious/Emeralds

### Testing

- Framework: pytest.
- Spec files live in `spec/` and end in `.spec.py`.
- `conftest.py` adds `src/` to `sys.path` so specs import by name.
- Run with `em test` (uses `pytest`).

### Code Style

- Run `em lint` to format and analyze sources using `ruff`.
- Prefer the standard library over adding dependencies.
- 2-space indent, final newline, LF, trimmed trailing whitespace.
- Max 80 chars/line. Follow existing script style.
- snake_case functions and variables; PascalCase classes.
- Double quotes for strings.
- Add focused tests for real behavior changes when practical.
