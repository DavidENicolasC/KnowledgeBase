You can create `.taurignore` files which work like regular `.gitignore` files:

```
build/
src/generated/*.rs
deny.toml
```

Are usually put in the `src-tauri` directory or [cargo workspace](https://doc.rust-lang.org/cargo/reference/workspaces.html) root folder. 

Currently, `tauri dev` looks for `.taurignore` files anywhere inside the common ancestor of the watched folders and the Cargo workspace root folder.