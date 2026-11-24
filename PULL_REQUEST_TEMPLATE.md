## Summary

<!-- Briefly describe what this PR changes and why. -->

## Related Issue

<!-- Link any related issue, e.g., Closes #123 -->

## Verification

- [ ] `cargo fmt --all -- --check`
- [ ] `cargo clippy --all-targets -- -D warnings`
- [ ] `cargo test`
- [ ] (WASM / Dioxus projects) `cargo clippy --target wasm32-unknown-unknown -- -D warnings`

## Checklist

- [ ] No `.unwrap()` / `.expect()` introduced in production code
- [ ] Documentation / README updated if user-facing behavior changed
- [ ] Light & Dark mode screenshots attached (for UI changes)
