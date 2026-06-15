You can set **`requireLiteralLeadingDot`** to **`false`** on the **object** `scope` (this widens what the WebView can load)

```
{
  "app": {
    "security": {
      "assetProtocol": {
        "enable": true,
        "scope": {
          "requireLiteralLeadingDot": false,
          "allow": ["$HOME/**/*"]
        }
      }
    }
  }
}
```