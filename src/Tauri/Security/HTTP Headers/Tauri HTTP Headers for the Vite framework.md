Those include [[Qwik]], [[React]], [[Solid]], [[Svelte]], and [[Vue]].

Include this on the [[Vite Configuration File]]. Sometimes this file is integrated into the frameworks configuration file, but the setup stays the same:
```
import { defineConfig } from 'vite';

export default defineConfig({
  // ...
  server: {
      // ...
      headers: {
        'Cross-Origin-Opener-Policy': 'same-origin',
        'Cross-Origin-Embedder-Policy': 'require-corp',
        'Timing-Allow-Origin': 'https://developer.mozilla.org, https://example.com',
        'Access-Control-Expose-Headers': 'Tauri-Custom-Header',
        'Tauri-Custom-Header': "key1 'value1' 'value2'; key2 'value3'"
      },
    },
})
```