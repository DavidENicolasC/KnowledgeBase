Return values that implements [`serde::Serialize`](https://docs.serde.rs/serde/trait.Serialize.html) are serialized to JSON when the response is sent to the frontend. This can slow down your application if you try to return a large data such as a file or a download HTTP response. To return array buffers in an optimized way, use [`tauri::ipc::Response`](https://docs.rs/tauri/2.0.0/tauri/ipc/struct.Response.html):

```rust
use tauri::ipc::Response;
#[tauri::command]
fn read_file() -> Response {
  let data = std::fs::read("/path/to/file").unwrap();
  tauri::ipc::Response::new(data)
}
```