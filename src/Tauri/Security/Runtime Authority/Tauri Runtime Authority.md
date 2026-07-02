Part of the [[Tauri Core]].

Holds all permissions, capabilities and scopes at runtime to enforce which window can access which command and passes scopes to commands.

Whenever a Tauri command is invoked:

1. Receives the invoke request, makes sure that the origin is allowed to actually use the requested command, checks if the origin is part of capabilities and if scopes are defined for the command and applicable then they are injected into the invoke request, which is then passed to the proper Tauri command.
2. If the origin is not allowed to call the command, will deny the request and the Tauri command is never invoked.