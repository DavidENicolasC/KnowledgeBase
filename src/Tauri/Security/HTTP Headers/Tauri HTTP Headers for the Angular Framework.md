Add the following to the [[Angular Configuration File]]:
```
{
  //...
  "projects":{
    //...
    "insert-project-name":{
      //...
      "architect":{
        //...
        "serve":{
          //...
          "options":{
            //...
            "headers":{
              "Cross-Origin-Opener-Policy": "same-origin",
              "Cross-Origin-Embedder-Policy": "require-corp",
              "Timing-Allow-Origin": "https://developer.mozilla.org, https://example.com",
              "Access-Control-Expose-Headers": "Tauri-Custom-Header",
              "Tauri-Custom-Header": "key1 'value1' 'value2'; key2 'value3'"
            }
          }
        }
      }
    }
  }
}
```