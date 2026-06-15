Use a list when you only need a fixed allow list and default glob behavior is enough:
```
{
  "app": {
    "security": {
      "assetProtocol": {
        "enable": true,
        "scope": ["$APPCACHE/**/*", "$RESOURCE/**/*"]
      }
    }
  }
}
```

In this form, you **cannot** set `requireLiteralLeadingDot`; for that, use the object form below.