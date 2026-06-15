 the deny scopes are merged into `deny-default`:

**plugins/fs/permissions/deny-default.toml**
```
[[set]]
identifier = "deny-default"
description = '''
This denies access to dangerous Tauri relevant files and
folders by default.
'''
permissions = ["deny-webview-data-linux", "deny-webview-data-windows"]
```

Afterwards deny and allow scopes are merged:
```
[[set]]
identifier = "scope-applocaldata-reasonable"
description = '''
This scope set allows access to the `APPLOCALDATA` folder and
subfolders except for linux,
while it denies access to dangerous Tauri relevant files and
folders by default on windows.
'''
permissions = ["scope-applocaldata-recursive", "deny-default"]
```

Where the two permissions above are permissions defined in the [[Including a scope type for a Tauri Command]]