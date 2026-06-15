By default, all commands that you registered in your app (using the [[tauri::Builder::invoke_handler function]] are allowed to be used by all the windows and webviews of the app. To change that, consider using [[AppManifest::commands]].

**src-tauri/build.rs**
```
fn main() {
    tauri_build::try_build(
        tauri_build::Attributes::new()
            .app_manifest(tauri_build::AppManifest::new().commands(&["your_command"])),
    )
    .unwrap();
}
```