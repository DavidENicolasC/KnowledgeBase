[[Tauri API]]s only work in your app window, so once you start using them you won’t be able to open your frontend in your system’s browser anymore.

If you prefer using your browser’s developer tooling, you must configure [[tauri-invoke-http]] to bridge Tauri API calls through a [[HTTP server]].