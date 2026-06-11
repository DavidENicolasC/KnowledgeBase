Holds everything together. It brings the runtimes, macros, utilities and API into one final product.

Reads the [[tauri.conf.json file]] at compile time to bring in features and undertake the actual configuration of the app (and even the `Cargo.toml` file in the project’s folder)

Handles script injection (for polyfills / prototype revision) at runtime, hosts the API for systems interaction, and even manages the updating process.