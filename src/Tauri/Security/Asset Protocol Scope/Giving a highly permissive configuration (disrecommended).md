If you intentionally need the broadest possible access **and** dot-prefixed segments, a maintainer-suggested shape looks like this. **This is not a default recommendation**; it increases exposure of hidden and sensitive files.

```
{
  "app": {
    "security": {
      "assetProtocol": {
        "enable": true,
        "scope": {
          "requireLiteralLeadingDot": false,
          "allow": ["**/*"]
        }
      }
    }
  }
}
```

Also, prefer narrow directories ($APPCACHE, $RESOURCE, a single app subfolder under $HOME, etc.) instead of broad $HOME/**/* or **/* unless you have a strong reason and understand the security tradeoffs.