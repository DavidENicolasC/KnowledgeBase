A way to intercept and modify Tauri API messages sent by the frontend before they get to Tauri Core, all with JavaScript.

Uses the [[Isolation Application]].

Provide a mechanism for developers to help protect their application from unwanted or malicious frontend calls to [[Tauri Core]].

The need rose out of [[Threat Models]].

Was mainly designed for [[Development Threat]]s.

[[Tauri]] highly recommends using this pattern.

You can utilize this to try and verify [[Inter-Process Comunication (IPC)]] inputs, to make sure they are within some expected parameters.

Tauri forces all IPC calls to Tauri Core to instead be routed through the sandboxed Isolation application first.

Once the message is ready to be passed to Tauri Core, it is encrypted using the browser’s [[SubtleCrypto]] implementation and passed back to the main frontend application. Once there, it is directly passed to Tauri Core.

New keys are generated each time your application is run.