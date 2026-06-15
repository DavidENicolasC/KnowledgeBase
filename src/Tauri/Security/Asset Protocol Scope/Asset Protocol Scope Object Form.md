Use an object when you need **deny** rules or to change **leading-dot** matching:
```
{
  "app": {
    "security": {
      "assetProtocol": {
        "enable": true,
        "scope": {
          "allow": ["$APPCACHE/**/*"],
          "deny": ["$APPCACHE/**/secrets/**"]
        }
      }
    }
  }
}
```

As `deny` is a [[Tauri Command Scope]], `deny` takes precedence over `allow` when both match.

You must take some [[Considerations about requiring leading dots on paths]] in account when you require leading dots on paths.