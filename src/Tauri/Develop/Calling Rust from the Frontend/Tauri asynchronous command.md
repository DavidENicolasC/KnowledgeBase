Are preferred in [[Tauri]] to perform heavy work in a manner that doesn’t result in UI freezes or slowdowns.

Are executed on a separate async task using [`async_runtime::spawn`](https://docs.rs/tauri/2.0.0/tauri/async_runtime/fn.spawn.html). Commands without the _async_ keyword are executed on the main thread unless defined with _#[tauri::command(async)]_.

Simply declare your [[Tauri Command]] as `async`.

Consider the [[Limitation about including borrowed arguments on an asynchronous function]].

Since invoking the command from JavaScript already returns a promise, it works just like any other command:

```javascript
invoke('my_custom_command', { value: 'Hello, Async!' }).then(() =>
  console.log('Completed!')
);
```