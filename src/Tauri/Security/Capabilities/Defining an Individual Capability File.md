The folllowing capability allows the main window use the default functionality of core plugins and the `window.setTitle` API.

**src-tauri/capabilities/default.json**
```
{
  "$schema": "../gen/schemas/desktop-schema.json",
  "identifier": "main-capability",
  "description": "Capability for the main window",
  "windows": ["main"],
  "permissions": [
    "core:path:default",
    "core:event:default",
    "core:window:default",
    "core:app:default",
    "core:resources:default",
    "core:menu:default",
    "core:tray:default",
    "core:window:allow-set-title"
  ]
}
```

These snippets are part of the [[Tauri Configuration File]].

 Is likely the most common configuration method, where the individual capabilities are inlined and only permissions are referenced by identifier.

```
{
  "app": {
    "security": {
      "capabilities": ["my-capability", "main-capability"]
    }
  }
}
```