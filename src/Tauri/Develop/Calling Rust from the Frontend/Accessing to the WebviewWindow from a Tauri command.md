Can access the `WebviewWindow` instance that invoked the message, by using a [[Tauri asynchronous command]]:
```rust
#[tauri::command]
async fn my_custom_command(webview_window: tauri::WebviewWindow) {
  println!("WebviewWindow: {}", webview_window.label());
}
```