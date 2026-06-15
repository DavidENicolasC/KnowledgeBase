Granular way to define (dis)allowed behavior of a [[Tauri Command]].

Are categorized into `allow` or `deny` scopes, where `deny` always supersedes the `allow` scope.

Their [[Command Scope Type]] needs be of any [[serde]] serializable type.

Is passed to the command and handling or properly enforcing is implemented by the command itself.

Developers need to ensure that there are no scope bypasses possible.