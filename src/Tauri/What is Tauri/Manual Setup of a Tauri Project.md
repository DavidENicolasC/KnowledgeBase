1. Create a new directory for your project and initialize the frontend. You can use plain HTML, CSS, and JavaScript, or any framework you prefer such as Next.js, Nuxt, Svelte, Yew, or Leptos. You just need a way of serving the app in your browser.
npm:
```
mkdir tauri-app
cd tauri-app
npm create vite@latest .
```
2. Install [[Tauri CLI Tool]] using your package manager of choice. If you are using `cargo` to install the Tauri CLI, you will have to install it globally.
npm:
```
npm install -D @tauri-apps/cli@latest
```
3. Determine the URL of your frontend development server. This is the URL that Tauri will use to load your content. For example, if you are using Vite, the default URL is: localhost:5173.
4. In your project directory, initialize Tauri:
npm:
```
npx tauri init
```
After running the command it will display a prompt asking you for different options. This will create a `src-tauri` directory in your project with the necessary Tauri configuration files:
```
✔ What is your app name? tauri-app
✔ What should the window title be? tauri-app
✔ Where are your web assets located? ..
✔ What is the url of your dev server? http://localhost:5173
✔ What is your frontend dev command? pnpm run dev
✔ What is your frontend build command? pnpm run build
```
5. Verify your Tauri app is working by running the development server. The command will compile the Rust code and open a window with your web content:
npm:
```
npx tauri dev
```