Is the package file used by [[Nodejs]].

If the frontend of your Tauri app is developed using Node.js-based technologies (such as `npm`, `yarn`, or `pnpm`) this file is used to configure the frontend dependencies and scripts.

```
{
  "scripts": {
    "dev": "command to start your app development mode",
    "build": "command to build your app frontend",
    "tauri": "tauri"
  },
  "dependencies": {
    "@tauri-apps/api": "^2.0.0",
    "@tauri-apps/cli": "^2.0.0"
  }
}
```

Consider the following [[About the scripts section in the Nodejs package file]].

Consider the following [[About the dependencies section in the Nodejs package file]].