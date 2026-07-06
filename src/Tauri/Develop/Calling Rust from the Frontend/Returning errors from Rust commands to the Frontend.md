Have the function return a `Result`:
```rust
#[tauri::command]
fn login(user: String, password: String) -> Result<String, String> {
  if user == "tauri" && password == "tauri" {
    // resolve
    Ok("logged_in".to_string())
  } else {
    // reject
    Err("invalid credentials".to_string())
  }
}
```

If the command returns an error, the promise will reject, otherwise, it resolves:

```Javascript
invoke('login', { user: 'tauri', password: '0j4rijw8=' })
  .then((message) => console.log(message))
  .catch((error) => console.error(error));
```