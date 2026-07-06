To create a command, just add a function and annotate it with `#[tauri::command]`.

Command names must be unique.

```rust
#[tauri::command]
fn my_custom_command() {
  println!("I was invoked from JavaScript!");
}
```

Commands defined in the `lib.rs` file cannot be marked as `pub` due to a limitation in the glue code generation. You will see an error like this if you mark it as a public function:
```rust
error[E0255]:
   = note: `__cmd__command_name` must be defined only once in the macro namespace of this module
```