JSON5 or TOML format can be enabled by adding the `config-json5` or `config-toml` feature flag (respectively) to the `tauri` and `tauri-build` dependencies in the [[Cargo Manifest File]].

Cargo.toml
```
[build-dependencies]
tauri-build = { version = "2.0.0", features = [ "config-json5" ] }

[dependencies]
tauri = { version = "2.0.0", features = [  "config-json5" ] }
```

Structure and values are the same across all formats, however, the formatting should be consistent with the respective file’s format.

JSON5:
```
{
  build: {
    devUrl: 'http://localhost:3000',
    // start the dev server
    beforeDevCommand: 'npm run dev',
  },
  bundle: {
    active: true,
    icon: ['icons/app.png'],
  },
  app: {
    windows: [
      {
        title: 'MyApp',
      },
    ],
  },
  plugins: {
    updater: {
      pubkey: 'updater pub key',
      endpoints: ['https://my.app.updater/{{target}}/{{current_version}}'],
    },
  },
}
```

TOML:
```
[build]
dev-url = "http://localhost:3000"
# start the dev server
before-dev-command = "npm run dev"

[bundle]
active = true
icon = ["icons/app.png"]

[[app.windows]]
title = "MyApp"

[plugins.updater]
pubkey = "updater pub key"
endpoints = ["https://my.app.updater/{{target}}/{{current_version}}"]
```

JSON5 and TOML supports comments, and TOML can use kebab-case for config names which are more idiomatic. Field names are case-sensitive in all 3 formats.