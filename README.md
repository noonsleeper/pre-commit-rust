# Rust hooks for pre-commit

[Rust](https://www.rust-lang.org) tools package for [pre-commit](https://pre-commit.com).

This is a fork of [doublify/pre-commit-rust](https://github.com/doublify/pre-commit-rust).

## Using rust tools with pre-commit

```yaml
-   repo: https://github.com/noonsleeper/pre-commit-rust
    rev: master
    hooks:
    -   id: fmt
    -   id: cargo-check
    -   id: clippy
```

## Passing arguments to rustfmt

```yaml
-   repo: https://github.com/noonsleeper/pre-commit-rust
    rev: master
    hooks:
    -   id: fmt
        args: ['--verbose', '--', '--edition', '2018' ]
```

> Note: Cargo fmt picks up "edition" automatically from Cargo.toml, so specificying this isn't necessary in most cases.
