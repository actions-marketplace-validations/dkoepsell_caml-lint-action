
---

# README for **`caml-lint-action`** (GitHub Action)

> ⚠️ This is **not an npm package**  
> This repository publishes a **GitHub Action**

```md
# CAML Lint GitHub Action

Run `caml-lint` automatically in GitHub Actions.

This action validates CAML files in CI so invalid or inconsistent narrative content never ships.

---

## What this is

- A GitHub Action
- Built on top of the `caml-lint` npm package
- Designed for zero-configuration use

---

## Usage

```yaml
- uses: dkoepsell/caml-lint-action@v0.1.0
  with:
    files: "adventures/**/*.caml.json"
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
