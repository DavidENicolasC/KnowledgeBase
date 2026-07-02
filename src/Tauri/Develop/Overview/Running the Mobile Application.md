By default, the mobile dev command tries to run your application on a connected device, and falls back to prompting you to select a simulator to use.

You can [[Provide a device or simulator name for running a Tauri Mobile Application]].

To define the run target upfront, you can provide the device or simulator name as an argument:
```
npm run tauri ios dev 'iPhone 15'
```

Alternatively, you can indicate to [[Use the native IDE when running a Tauri Mobile Application]].

Also, consider the following for [[Running a Tauri Application on a physical iOS device]].