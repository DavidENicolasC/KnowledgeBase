An option in the tauri config file:

```
{
  "build": {
    "removeUnusedCommands": true
  }
}
```

to remove commands that’re never allowed in your capability files (ACL), so you don’t have to pay for what you don’t use.

To maximize the benefit of this, only include commands that you use in the ACL instead of using `defaults`s

This feature requires `tauri@2.4`, `tauri-build@2.1`, `tauri-plugin@2.1` and `tauri-cli@2.4`

This won’t be accounting for dynamically added ACLs at runtime so make sure to check it when using this.

`tauri-cli` will communicate with `tauri-build` and the build script of `tauri`, `tauri-plugin` through an environment variable and let them generate a list of allowed commands from the ACL, this will then be used by the `generate_handler` macro to remove unused commands based on that

An internal detail is this environment variable is currently `REMOVE_UNUSED_COMMANDS`, and it’s set to project’s directory, usually the `src-tauri` directory, this is used for the build scripts to find the capability files, and although it’s not encouraged, you can still set this environment variable yourself if you can’t or don’t want to use `tauri-cli` to get this to work (**do note that as this is an implementation detail, we don’t guarantee the stability of it**)