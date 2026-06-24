Entries in [[Tauri Configuration File]] describe **static** allow/deny patterns, like [[Command Scope Type]]s. They do not replace runtime workflows where the user picks arbitrary folders or files (for example with the **dialog** plugin): those paths may need to be **persisted** across restarts using the [[persisted-scope Tauri plugin]].

Enable its **`protocol-asset`** Cargo feature in the [[Cargo Profile Configuration]] file `src-tauri/Cargo.toml`, for example:

```
tauri-plugin-persisted-scope = { version = "2", features = ["protocol-asset"] }
```

Register **`tauri_plugin_fs`** before **`tauri_plugin_persisted_scope`** as described in the plugin guide.