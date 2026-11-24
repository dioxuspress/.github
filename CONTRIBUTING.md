# Contributing to DioxusPress

Thank you for your interest in contributing to the [**DioxusPress**](https://github.com/dioxuspress) ecosystem! All repositories under this organization are pure-Rust projects licensed under MIT.

## Before You Start

1. Check existing issues and pull requests in the target repository to avoid duplicate work.
2. For large features or architectural changes, open an issue first to align on design and scope.
3. Fork the repository and create a focused branch from `main` (for example, `feat/your-feature` or `fix/your-bug`).

## Engineering Baseline

Across `dioxuspress` repositories, we enforce a consistent Rust quality bar:

- **Formatting**: Run `cargo fmt --all -- --check` (every repository includes a `rustfmt.toml` with 2-space indentation).
- **Zero-warning Clippy**: Run `cargo clippy --all-targets -- -D warnings`. For Dioxus WASM projects, also verify `cargo clippy --target wasm32-unknown-unknown -- -D warnings`.
- **Error Handling**: Avoid `.unwrap()` and `.expect()` in production code; propagate errors with `Result` / `?` or handle them explicitly.
- **Strict CSP for Web/WASM**: Avoid `document::eval` or `'unsafe-eval'` JavaScript workarounds; prefer pure-Rust Dioxus rendering and typed web-sys APIs.
- **Tests**: Add or update unit/integration tests covering your changes and verify `cargo test` passes locally.

## Commit & Pull Request Guidelines

- Follow [Conventional Commits](https://www.conventionalcommits.org/) for commit headers (`feat:`, `fix:`, `docs:`, `refactor:`, `perf:`, `test:`, `chore:`).
- Keep pull requests focused on a single logical change.
- Fill out the PR checklist, including the exact verification commands you ran.
- For UI or visual changes, attach before/after screenshots in both Light and Dark themes.

## License

By contributing to any repository under `dioxuspress`, you agree that your contributions will be licensed under the MIT License.
