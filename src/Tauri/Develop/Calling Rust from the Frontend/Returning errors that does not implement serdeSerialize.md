In simple scenarios you can use `map_err` to convert these errors to `String`:
```
#[tauri::command]
fn my_custom_command() -> Result<(), String> {
  std::fs::File::open("path/to/file").map_err(|err| err.to_string())?;
  // Return `null` on success
  Ok(())
}
```

You may want to create your own [[Rust custom error type]] which implements `serde::Serialize`.

 In the following example, we use the [`thiserror`](https://github.com/dtolnay/thiserror) crate to help create the error type. It allows you to turn enums into error types by deriving the `thiserror::Error` trait.
```rust
// create the error type that represents all errors possible in our program
#[derive(Debug, thiserror::Error)]
enum Error {
  #[error(transparent)]
  Io(#[from] std::io::Error)
}

// we must manually implement serde::Serialize
impl serde::Serialize for Error {
  fn serialize<S>(&self, serializer: S) -> Result<S::Ok, S::Error>
  where
    S: serde::ser::Serializer,
  {
    serializer.serialize_str(self.to_string().as_ref())
  }
}

#[tauri::command]
fn my_custom_command() -> Result<(), Error> {
  // This will return an error
  std::fs::File::open("path/that/does/not/exist")?;
  // Return `null` on success
  Ok(())
}
```