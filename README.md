# rustfumi [![linux](https://github.com/rust-lang/rustfmt/actions/workflows/linux.yml/badge.svg?event=push)](https://github.com/rust-lang/rustfmt/actions/workflows/linux.yml) [![mac](https://github.com/rust-lang/rustfmt/actions/workflows/mac.yml/badge.svg?event=push)](https://github.com/rust-lang/rustfmt/actions/workflows/mac.yml) [![windows](https://github.com/rust-lang/rustfmt/actions/workflows/windows.yml/badge.svg?event=push)](https://github.com/rust-lang/rustfmt/actions/workflows/windows.yml) [![crates.io](https://img.shields.io/crates/v/rustfmt-nightly.svg)](https://crates.io/crates/rustfmt-nightly)

A fork of rustfmt that merges a few useful pull requests.

rustfmt's PR review queue is heavily backed up. For example,
[let-else statements were stabilized in November 2022](https://ehuss.github.io/rust/all-one-page/all.html#version-1650-2022-11-03)
and [added to the style guide in February 2023](https://github.com/rust-lang/rust/pull/107312),
but [rust-lang/rustfmt#5690](https://github.com/rust-lang/rustfmt/pull/5690) has remained unmerged for more than 3 months.
The PR is [apparently being discussed through other channels](https://github.com/rust-lang/rustfmt/pull/5690#issuecomment-1481642464),
but to casual observers, the current status of the PR is entirely unclear.

`rustfumi` resolves this by merging this PR, along with a few others. As a consequence, however,
`rustfumi` is inherently unstable and likely contains buggy, incomplete features. rustfmt's
guarantees of stability and (alleged) idempotency are **completely off the table**.

## Quick start

Nightly is required to build `rustfumi`.

To test:

```sh
cargo +nightly test
```

To install:

```sh
cargo install --path .
cargo install --path . --bin cargo-fumi
```

To run on a cargo project in the current working directory:

```sh
cargo fumi
```

For more information, see [rustfmt's README.md](https://github.com/rust-lang/rustfmt/blob/master/README.md).

## License

`rustfumi` is distributed under the terms of both the MIT license and the
Apache License (Version 2.0).

See [LICENSE-APACHE](LICENSE-APACHE) and [LICENSE-MIT](LICENSE-MIT) for details.

[rust]: https://github.com/rust-lang/rust
[fmt rfcs]: https://github.com/rust-dev-tools/fmt-rfcs
[style guide]: https://github.com/rust-dev-tools/fmt-rfcs/blob/master/guide/guide.md
