 Used to ensure that permissions can be re-used and have unique names.

We refer to the plugin crate name without the `tauri-plugin-` prefix. Is meant as namespacing to reduce likelihood of naming conflicts.

Plugin prefix `tauri-plugin-` will be automatically prepended to the identifier of plugins at compile time and is not required to be manually specified

 Are limited to ASCII lower case alphabetic characters `[a-z]` and the maximum length of the identifier is currently limited to `116`.