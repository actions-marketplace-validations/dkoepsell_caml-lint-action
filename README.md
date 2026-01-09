# caml-lint-action

A tiny GitHub Action that runs `caml-lint` in CI.

## Usage

```yaml
name: caml

on:
  push:
  pull_request:

jobs:
  caml-lint:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: "20"
      - uses: dkoepsell/caml-lint-action@v0.1.0
        with:
          files: "examples/*.caml.json"
```

## Inputs

- `files`: Glob of CAML files to lint (default: `examples/*.caml.json`)
- `json`: Set to `true` to emit JSON output

## License

MIT
