When [[Using a development server]], You must configure it to listen to a particular address provided by the Tauri CLI, defined in the `TAURI_DEV_HOST` environment variable.

This address is either a public network address (which is the default behavior) or the actual iOS device TUN address — which is more secure, but currently needs [[Xcode]] to connect to the device.

You must open Xcode before running the dev command and ensure your device is connected via network in the Window > Devices and Simulators menu. Then you must run `tauri ios dev --force-ip-prompt` to select the iOS device address (an IPv6 address ending with **::2**).

To make your development server listen on the correct host to be accessible by the iOS device, you must tweak its configuration to use the `TAURI_DEV_HOST` value if it has been provided. Here is an example configuration for Vite:

```
import { defineConfig } from 'vite';

const host = process.env.TAURI_DEV_HOST;

// https://vitejs.dev/config/
export default defineConfig({
  clearScreen: false,
  server: {
    host: host || false,
    port: 1420,
    strictPort: true,
    hmr: host
      ? {
          protocol: 'ws',
          host,
          port: 1421,
        }
      : undefined,
  },
});
```