You can do it with the `rename_all` attribute:
```Javascript
#[tauri::command(rename_all = "snake_case")]
fn my_custom_command(invoke_message: String) {}
```

And the corresponding Javascript:
```Javascript
invoke('my_custom_command', { invoke_message: 'Hello!' });
```