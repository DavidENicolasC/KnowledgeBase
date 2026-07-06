You cannot simply include borrowed arguments in the signature of a [[Tauri asynchronous command]] function.
Some common examples of types like this are `&str` and `State<'_, Data>`.

These are your two main options:
1. Convert the type, such as `&str` to a similar type that is not borrowed, such as `String`. This may not work for all types, for example `State<'_, Data>`.
```rust
// Declare the async function using String instead of &str, as &str is borrowed and thus unsupported
#[tauri::command]
async fn my_custom_command(value: String) -> String {
  // Call another async function and wait for it to finish
  some_async_function().await;
  value
}
```

2. Wrap the return type in a [`Result`](https://doc.rust-lang.org/std/result/index.html). This one is a bit harder to implement, but works for all types.
Use the return type `Result<a, b>`, replacing `a` with the type you wish to return, or `()` if you wish to return `null`, and replacing `b` with an error type to return if something goes wrong, or `()` if you wish to have no optional error returned. For example:

- `Result<String, ()>` to return a String, and no error.
- `Result<(), ()>` to return `null`.
- `Result<bool, Error>` to return a boolean or an error as shown in the [[Returning errors from Rust commands to the Frontend]] section above.
```rust
// Return a Result<String, ()> to bypass the borrowing issue
#[tauri::command]
async fn my_custom_command(value: &str) -> Result<String, ()> {
  // Call another async function and wait for it to finish
  some_async_function().await;
  // Note that the return value must be wrapped in `Ok()` now.
  Ok(format!(value))
}
```