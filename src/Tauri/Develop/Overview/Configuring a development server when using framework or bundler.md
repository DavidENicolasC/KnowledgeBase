If you are using a UI framework or JavaScript bundler, you likely have access to a development server that will speed up your development process, so if you haven’t configured your app’s dev URL and script that starts it, you can do so via the [devUrl](https://v2.tauri.app/reference/config/#devurl) and [beforeDevCommand](https://v2.tauri.app/reference/config/#beforedevcommand) config values:

```
{
  "build": {
    "devUrl": "http://localhost:3000",
    "beforeDevCommand": "npm run dev"
  }
}
```