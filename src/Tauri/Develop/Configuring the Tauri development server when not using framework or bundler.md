Otherwise, if you are not using a UI framework or module bundler, you can point Tauri to your frontend source code and the Tauri CLI will start a development server for you:
```
{
  "build": {
    "frontendDist": "./src"
  }
}
```

In this example, the `src` folder must include an `index.html` file along with any other assets loaded by your frontend.