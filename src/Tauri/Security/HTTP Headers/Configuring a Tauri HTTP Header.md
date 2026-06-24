- with a string
- with an array of strings
- with an object/key-value, where the values must be strings
- with null
[[Tauri HTTP Header]] values are always converted to strings for the actual response.

Depending on how the configuration file looks, some header values need to be [[Tauri HTTP Composed Header]]s.

```
{
 //...
  "app":{
    //...
    "security": {
      //...
      "headers": {
        "Cross-Origin-Opener-Policy": "same-origin",
        "Cross-Origin-Embedder-Policy": "require-corp",
        "Timing-Allow-Origin": [
          "https://developer.mozilla.org",
          "https://example.com",
        ],
        "X-Content-Type-Options": null, // gets ignored
        "Access-Control-Expose-Headers": "Tauri-Custom-Header",
        "Tauri-Custom-Header": {
          "key1": "'value1' 'value2'",
          "key2": "'value3'"
        }
      },
      // notice how the CSP is not defined under headers
      "csp": "default-src 'self'; connect-src ipc: http://ipc.localhost",
    }
  }
}
```

In this example [[Cross-Origin-Opener-Policy]] and [[Cross-Origin-Embedder-Policy]] are set to allow for the use of [[SharedArrayBuffer]]. [[Timing-Allow-Origin]] grants scripts loaded from the listed websites to access detailed network timing data via the [[Resource Timing API]].

```
access-control-allow-origin:  http://tauri.localhost
access-control-expose-headers: Tauri-Custom-Header
content-security-policy: default-src 'self'; connect-src ipc: http://ipc.localhost; script-src 'self' 'sha256-Wjjrs6qinmnr+tOry8x8PPwI77eGpUFR3EEGZktjJNs='
content-type: text/html
cross-origin-embedder-policy: require-corp
cross-origin-opener-policy: same-origin
tauri-custom-header: key1 'value1' 'value2'; key2 'value3'
timing-allow-origin: https://developer.mozilla.org, https://example.com
```