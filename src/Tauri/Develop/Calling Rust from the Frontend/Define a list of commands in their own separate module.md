When defining commands in a separate module they should be marked as `pub`.

The command name is not scoped to the module so they must be unique even between modules.

As an example let’s define a command in the `src-tauri/src/commands.rs` file:

```rust
#[tauri::command]
pub fn my_custom_command() {
  println!("I was invoked from JavaScript!");
}
```

In the `lib.rs` file, define the module and provide the list of your commands accordingly;
```rust
mod commands;

#[cfg_attr(mobile, tauri::mobile_entry_point)]
pub fn run() {
  tauri::Builder::default()
    .invoke_handler(tauri::generate_handler![commands::my_custom_command])
    .run(tauri::generate_context!())
    .expect("error while running tauri application");
}
```

Note the `commands::` prefix in the command list, which denotes the full path to the command function.