[[Tauri]] can read a platform-specific configuration from:

- `tauri.linux.conf.json` or `Tauri.linux.toml` for Linux
- `tauri.windows.conf.json` or `Tauri.windows.toml` for Windows
- `tauri.macos.conf.json` or `Tauri.macos.toml` for macOS
- `tauri.android.conf.json` or `Tauri.android.toml` for Android
- `tauri.ios.conf.json` or `Tauri.ios.toml` for iOS
The platform-specific configuration file gets merged with the main configuration object following the [[JSON Merge Patch (RFC 7396)]] specification.

For example, given the following base `tauri.conf.json`:
```
{
  "productName": "MyApp",
  "bundle": {
    "resources": ["./resources"]
  },
  "plugins": {
    "deep-link": {}
  }
}
```

And the given `tauri.linux.conf.json`:
```
{
  "productName": "my-app",
  "bundle": {
    "resources": ["./linux-assets"]
  },
  "plugins": {
    "cli": {
      "description": "My app",
      "subcommands": {
        "update": {}
      }
    },
    "deep-link": {}
  }
}
```

The resolved configuration for Linux would be the following object:
```
{
  "productName": "my-app",
  "bundle": {
    "resources": ["./linux-assets"]
  },
  "plugins": {
    "cli": {
      "description": "My app",
      "subcommands": {
        "update": {}
      }
    },
    "deep-link": {}
  }
}
```