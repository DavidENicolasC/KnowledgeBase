Tauri CLI allows you to extend the Tauri configuration when running one of the `dev`, `android dev`, `ios dev`, `build`, `android build`, `ios build` or `bundle` commands.

The configuration extension can be provided by the `--config` argument either as a raw JSON string or as a path to a JSON file.

Tauri uses the [[JSON Merge Patch (RFC 7396)]] specification to merge the provided configuration value with the originally resolved configuration object.

This mechanism can be used to define multiple flavours of your application.

To distribute a completely isolated _beta_ application you can use this feature to configure a separate application name and identifier:
```
{
  "productName": "My App Beta",
  "identifier": "com.myorg.myappbeta"
}
```

And use it to build the app with, for example, [[npm]]:
```
npm run tauri build -- --config src-tauri/tauri.beta.conf.json
```