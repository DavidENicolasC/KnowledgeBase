If you want the processor to fail when the document contains a missing attribute, set this attribute to warn and pass the `--failure-level=WARN` option to the CLI.

```
$ asciidoctor -a attribute-missing=warn --failure-level=WARN doc.adoc
```