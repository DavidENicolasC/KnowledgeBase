![Diagram](https://tauri.app/d2/docs/concept/process-model-0.svg)
Each [[Tauri application]] has one, which acts as the application’s entry point and is the only component with full access to the operating system.

Its primary responsibility is to use that access to create and orchestrate application windows, system-tray menus, or notifications, 

Implements the necessary cross-platform abstractions to make this easy

Routes all [[Inter-Process Communication]].

Manage the global state, such as settings or database connections.