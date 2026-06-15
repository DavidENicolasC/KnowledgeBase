Are described as follows:
```
[[permission]]
identifier = "my-identifier"
description = "This describes the impact and more."
commands.allow = [
    "read_file"
]

[[scope.allow]]
my-scope = "$HOME/*"

[[scope.deny]]
my-scope = "$HOME/secret"
```

Can enable commands to be accessible in the frontend of a Tauri application.
Can map scopes to commands and defines which commands are enabled.
Can enable or deny certain commands, define scopes or combine both.

You must reference the permission in a [[Capability]].

Can be grouped under a [[Tauri Permission Set]].

Use a [[Tauri Permission Identifier]].

Use the [[Tauri Permission Syntax]].

Only can be defined in `toml`.