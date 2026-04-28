[[Tauri]] acts as a [[Static Web Host]]. You need to provide Tauri with a folder containing some mix of HTML, CSS, Javascript and possibly WASM that can be served to the webview Tauri provides.

The way it builds is that you would compile your JavaScript project to static files first, and then compile the Rust project that will bundle those static files in, so the JavaScript project setup is basically the same as if you were to build a static website. [[Tauri Project Structure]]

If you want to work with Rust code only, simply remove everything else and use the `src-tauri/` folder as your top level project or as a member of your Rust workspace.