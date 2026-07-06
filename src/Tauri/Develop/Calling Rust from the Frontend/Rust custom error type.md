A custom error type has the advantage of making all possible errors explicit so readers can quickly identify what errors can happen.

It also gives you full control over the way your error type gets serialized. In the above example, we simply returned the error message as a string, but you could assign each error a code so you could more easily map it to a similar looking TypeScript error enum for example:
```rust
#[derive(Debug, thiserror::Error)]
enum Error {
  #[error(transparent)]
  Io(#[from] std::io::Error),
  #[error("failed to parse as string: {0}")]
  Utf8(#[from] std::str::Utf8Error),
}

#[derive(serde::Serialize)]
#[serde(tag = "kind", content = "message")]
#[serde(rename_all = "camelCase")]
enum ErrorKind {
  Io(String),
  Utf8(String),
}

impl serde::Serialize for Error {
  fn serialize<S>(&self, serializer: S) -> Result<S::Ok, S::Error>
  where
    S: serde::ser::Serializer,
  {
    let error_message = self.to_string();
    let error_kind = match self {
      Self::Io(_) => ErrorKind::Io(error_message),
      Self::Utf8(_) => ErrorKind::Utf8(error_message),
    };
    error_kind.serialize(serializer)
  }
}

#[tauri::command]
fn read() -> Result<Vec<u8>, Error> {
  let data = std::fs::read("/path/to/file")?;
  Ok(data)
}
```

In your frontend you now get a `{ kind: 'io' | 'utf8', message: string }` error object:
```Javascript
type ErrorKind = {
  kind: 'io' | 'utf8';
  message: string;
};

invoke('read').catch((e: ErrorKind) => {});
```