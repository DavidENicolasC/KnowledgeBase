Tries to be as compatible as possible with existing frontend projects.

Tries to require nothing additional to what an existing web frontend might use inside a browser.

Not _**everything**_ that works in existing browser applications will work out-of-the-box.

Doesn’t require a configuration option to be set.

To explicitly set it, you can use the `app > security > pattern` object in the `tauri.conf.json` configuration file.

```
{
  "app": {
    "security": {
      "pattern": {
        "use": "brownfield"
      }
    }
  }
}
```