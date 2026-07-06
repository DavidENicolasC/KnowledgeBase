You need to write your functions as follows for use, for example, the [[Mock runtime]].
```rust
use tauri::{AppHandle, GlobalShortcutManager, Runtime, WebviewWindow};

#[tauri::command]
async fn my_custom_command<R: Runtime>(app_handle: AppHandle<R>, webview_window: WebviewWindow<R>) {
  let app_dir = app_handle.path().app_dir();
  app_handle
    .global_shortcut_manager()
    .register("CTRL + U", move || {});
  println!("WebviewWindow: {}", webview_window.label());
}
```