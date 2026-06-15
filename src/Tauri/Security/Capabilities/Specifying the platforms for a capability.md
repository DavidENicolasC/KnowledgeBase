By default the capability is applied to all targets, but you can select a subset of the `linux`, `macOS`, `windows`, `iOS` and `android` targets.

The platforms can be specified by defining the `platforms` array.

**src-tauri/capabilities/desktop.json**
```
{
  "$schema": "../gen/schemas/desktop-schema.json",
  "identifier": "desktop-capability",
  "windows": ["main"],
  "platforms": ["linux", "macOS", "windows"],
  "permissions": ["global-shortcut:allow-register"]
}
```

**src-tauri/capabilities/mobile.json**
```
{
  "$schema": "../gen/schemas/mobile-schema.json",
  "identifier": "mobile-capability",
  "windows": ["main"],
  "platforms": ["iOS", "android"],
  "permissions": [
    "nfc:allow-scan",
    "biometric:allow-authenticate",
    "barcode-scanner:allow-scan"
  ]
}
```