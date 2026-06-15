`assetProtocol.scope` uses the same **`FsScope`** type as filesystem-related configuration elsewhere: either a **JSON array** of allowed glob patterns, or a **JSON object** with `allow`, optional `deny`, and optional `requireLiteralLeadingDot`. 

Patterns may start with a **base directory variable** (for example `$HOME`, `$CACHE`, `$APPCACHE`, `$APPDATA`, `$RESOURCE`)

You must set **`enable`** to `true` and define a **`scope`** that lists which filesystem paths may be exposed. Paths resolved at runtime must match that scope, or the WebView will refuse the load (often with an error such as “asset protocol not configured to allow the path”).

Are defined by [[Defining an Asset Protocol Scope]].