## Project Context

### Stack

- Go project managed by Emeralds (`em` CLI) on top of `go mod`.
- `go.mod` is the source of truth for dependencies.
- `em.json` wraps it and delegates to `go`.
- Compiler config comes from `em.json`.
- Emeralds documentation: https://github.com/Oblivious-Oblivious/Emeralds

### Testing

- Framework: Go's built-in `testing` package.
- Spec files live in `spec/` and end in `.spec.go`; `em test` runs them via `go test`.
- Run with `em test`.

### Code Style

- Run `em lint` to format sources using `gofmt`.
- Prefer the standard library over adding dependencies.
- 2-space indent, final newline, LF, trimmed trailing whitespace.
- Max 80 chars/line. Follow existing script style.
- Add focused tests for real behavior changes when practical.
