```
tauri-plugin
├── README.md
├── src
│  └── lib.rs
├── build.rs
├── Cargo.toml
├── permissions
│  └── <identifier>.json/toml
│  └── default.json/toml
```

Default permission is handled in a special way, as it is automatically added to the application configuration, as long as the Tauri CLI is used to add plugins to a Tauri application.