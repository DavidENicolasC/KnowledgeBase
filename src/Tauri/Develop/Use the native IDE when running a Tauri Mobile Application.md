To open the mobile IDE instead of running on a connected device or simulator, use the `--open` flag:

```
npm run tauri [android|ios] dev --open
```

The Tauri CLI process **must** be running and **cannot** be killed. It is recommended to use the `tauri [android|ios] dev --open` command and keep the process alive until you close the IDE.