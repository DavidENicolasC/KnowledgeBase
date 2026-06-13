1. Tauri’s IPC handler receives a message
2. IPC handler -> Isolation application
3. `[sandbox]` Isolation application hook runs and potentially modifies the message
4. `[sandbox]` Message is encrypted with AES-GCM using a runtime-generated key
5. `[encrypted]` Isolation application -> IPC handler
6. `[encrypted]` IPC handler -> Tauri Core