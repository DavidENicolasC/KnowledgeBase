Define which [[Tauri Permission]]s are granted or denied for which windows or webviews.

Can affect multiple windows and webviews and these can be referenced in multiple capabilities.

Can be written in `json`/`json5` or `toml` inside the `src-tauri/capabilities` directory. All capabilities in this directory are automatically enabled by default.

Once are explicitly enabled in the [[Tauri Configuration File]], only these are used in the application build.

Can be platform-specific by [[Specifying the platforms for a capability]].

Can manage the access from remote sources to certain [[Tauri Command]]s by [[Specifying the Remote API access]].