It´s `Cargo.toml`.

Used to declare [[Rust crate]]s your app depends on, metadata about your app, and other [[Rust]]-related features.

```
[package]
name = "app"
version = "0.1.0"
description = "A Tauri App"
authors = ["you"]
license = ""
repository = ""
default-run = "app"
edition = "2021"
rust-version = "1.57"

[build-dependencies]
tauri-build = { version = "2.0.0" }

[dependencies]
serde_json = "1.0"
serde = { version = "1.0", features = ["derive"] }
tauri = { version = "2.0.0", features = [ ] }
```

The most important parts to take note of are the `tauri-build` and `tauri` dependencies. Generally, they must both be on the same latest minor versions as the [[Tauri CLI]], but this is not strictly required.

Cargo version numbers use [[Semantic Versioning]]. Running `cargo update` in the `src-tauri` folder will pull the latest available Semver-compatible versions of all dependencies. For example, if you specify `2.0.0` as the version for `tauri-build`, Cargo will detect and download version `2.0.1` because it is the latest Semver-compatible version available.

If you want to use a specific crate version you can use exact versions instead by prepending `=` to the version number of the dependency:

```
tauri-build = { version = "=2.0.0" }
```

