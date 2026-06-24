Add the following to the [[Next.js Configuration File]]:
```
module.exports = {
  //...
  async headers() {
    return [
      {
        source: '/*',
        headers: [
          {
            key: 'Cross-Origin-Opener-Policy',
            value: 'same-origin',
          },
          {
            key: 'Cross-Origin-Embedder-Policy',
            value: 'require-corp',
          },
          {
            key: 'Timing-Allow-Origin',
            value: 'https://developer.mozilla.org, https://example.com',
          },
          {
            key: 'Access-Control-Expose-Headers',
            value: 'Tauri-Custom-Header',
          },
          {
            key: 'Tauri-Custom-Header',
            value: "key1 'value1' 'value2'; key2 'value3'",
          },
        ],
      },
    ]
  },
}
```