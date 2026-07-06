```rust
#[tauri::command]
fn my_custom_command(invoke_message: String) {
  println!("I was invoked from JavaScript, with this message: {}", invoke_message);
}
```

Arguments should be passed as a JSON object with camelCase keys:
```Javascript
invoke('my_custom_command', { invokeMessage: 'Hello!' });
```

Can be of any type, as long as they implement [`serde::Deserialize`](https://docs.serde.rs/serde/trait.Deserialize.html).

You can [[Use snake_case for the arguments]].