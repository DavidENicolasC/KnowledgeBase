a [[Foreign Function Interface]]-like abstraction on top of [[Inter-Process Comunication (IPC)]] messages.

The primary API, `invoke`, is similar to the browser’s `fetch` API and allows the Frontend to invoke Rust functions, pass arguments, and receive data.

All arguments and return data must be serializable to JSON as this mechanism uses a [[JSON-RPC]] like protocol under the hood to serialize requests and responses.

They do not share the same security pitfalls as real [[Foreign Function Interface]]s do, as still use [[Message Passing]] under the hood.