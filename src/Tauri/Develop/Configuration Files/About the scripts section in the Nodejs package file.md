It’s common to use this section to store the commands used to launch and build the frontend used by your Tauri application.
```
"scripts": {
	"dev": "command to start your app development mode",
	"build": "command to build your app frontend",
	"tauri": "tauri"
}
```

The above `package.json` file specifies the `dev` command that you can run using `yarn dev` or `npm run dev` to start the frontend framework and the `build` command that you can run using `yarn build` or `npm run build` to build your frontend’s Web assets to be added by Tauri in production.

The most convenient way to use these scripts is [[Hooking nodejs package scripts via the Tauri configuration file]].

Is only needed when using `npm`.