You can use the `separator` [[Block Attribute]].
```
[separator=::]
= Main Title:: Subtitle
```

You can also use the `title-separator` [[Document Attribute]]. Can also be assigned by CLI.
```
= Main Title:: Subtitle
:title-separator: ::


$ asciidoctor -a title-separator=:: document.adoc
```