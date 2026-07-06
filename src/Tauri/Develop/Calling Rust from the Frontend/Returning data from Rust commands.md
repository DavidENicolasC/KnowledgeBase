```rust
#[tauri::command]
fn my_custom_command() -> String {
  "Hello from Rust!".into()
}
```

The `invoke` function returns a promise that resolves with the returned value:
```
invoke('my_custom_command').then((message) => console.log(message));
```

Can be of any type, as long as it implements [`serde::Serialize`](https://docs.serde.rs/serde/trait.Serialize.html). everything returned from commands must implement [`serde::Serialize`](https://docs.serde.rs/serde/trait.Serialize.html), including [[Returning errors from Rust commands to the Frontend]].

Consider [[Returning data as array buffers]].