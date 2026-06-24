header defined in the configuration gets sent along the responses to the webview. This doesn’t include IPC messages and error responses. To be more specific, every response sent via the `get_response` function in  [[Rust Configuration Reference]] will include those headers.

Are limited to:

- [[Access-Control-Allow-Credentials]]
- [[Access-Control-Allow-Headers]]
- [[Access-Control-Allow-Methods]]
- [[Access-Control-Expose-Headers]]
- [[Access-Control-Max-Age]]
- [[Cross-Origin-Embedder-Policy]]
- [[Cross-Origin-Opener-Policy]]
- [[Cross-Origin-Resource-Policy]]
- [[Permissions-Policy]]
- [[Service-Worker-Allowed]]
- [[Timing-Allow-Origin]]
- [[X-Content-Type-Options]]
- [[Tauri-Custom-Header]]
[[Content Security Policy (CSP)]] is not defined here.

The following are the headers to add for the Javascript/Typescript side:
- [[Tauri HTTP Headers for the Vite framework]]
- [[Tauri HTTP Headers for the Angular Framework]]
- [[Tauri HTTP Headers for the Nuxt Framework]]
- [[Tauri HTTP Headers for the Next.js Framework]]

And the following are for the Rust side:
-  [[Tauri HTTP Headers for Yew and Leptos Frameworks]]