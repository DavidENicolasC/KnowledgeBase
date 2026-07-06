The recommended mechanism for streaming data such as [[Streamed HTTP Response]]s to the frontend.

The following example reads a file and notifies the frontend of the progress in chunks of 4096 bytes by using a [[Tauri asynchronous command]]:
```rust
use tokio::io::AsyncReadExt;

#[tauri::command]
async fn load_image(path: std::path::PathBuf, reader: tauri::ipc::Channel<&[u8]>) {
  // for simplicity this example does not include error handling
  let mut file = tokio::fs::File::open(path).await.unwrap();

  let mut chunk = vec![0; 4096];

  loop {
    let len = file.read(&mut chunk).await.unwrap();
    if len == 0 {
      // Length of zero means end of file.
      break;
    }
    reader.send(&chunk).unwrap();
  }
}
```