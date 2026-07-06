Both take a generic parameter `R: Runtime`, when the `wry` feature is enabled in `tauri` (which is enabled by default), we default the generic to the `Wry` runtime so you can use it directly.

Consider the following if you want to [[Use a different runtime for WebviewWindow and AppHandle]].