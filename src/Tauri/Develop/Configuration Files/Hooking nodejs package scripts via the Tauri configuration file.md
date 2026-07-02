You can do this via the [[Tauri CLI]] on the [[Tauri Configuration File]], and using the  [[beforeDevCommand]] and [[beforeBuildCommand]] hooks.

tauri.conf.json
```
{
  "build": {
    "beforeDevCommand": "yarn dev",
    "beforeBuildCommand": "yarn build"
  }
}
```