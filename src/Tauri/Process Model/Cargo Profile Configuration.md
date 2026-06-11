Dependent on whether you use the stable or nightly Rust toolchain the options available to you differ a bit. It’s recommended you stick to the stable toolchain unless you’re an advanced user.

```
[profile.dev]
incremental = true # Compile your binary in smaller steps.

[profile.release]
codegen-units = 1 # Allows LLVM to perform better optimization.
lto = true # Enables link-time-optimizations.
opt-level = "s" # Prioritizes small binary size. Use `3` if you prefer speed.
panic = "abort" # Higher performance by disabling panic handlers.
strip = true # Ensures debug symbols are removed.
```

Small reference:
- incremental - Compile your binary in smaller steps.
- codegen-units: - Speeds up compile times at the cost of compile time optimizations.
- lto - Enables link time optimizations.
- opt-level - Determines the focus of the compiler. Use `3` to optimize performance, `z` to optimize for size, and `s` for something in-between.
- panic - Reduce size by removing panic unwinding.
- strip - Strip either symbols or debuginfo from a binary.
- rpath - Assists in finding the dynamic libraries the binary requires by hard coding information into the binary.
- trim-paths - Removes potentially privileged information from binaries.
- rustflags - Sets Rust compiler flags on a profile by profile basis.
    - `-Cdebuginfo=0`: Whether debuginfo symbols should be included in the build.
    - `-Zthreads=8`: Increases the number of threads used during compilation.