Form a controlled vocabulary that can be used to navigate the document by keyword starting from an index.

List the [[Index Term]]s.

Only [[Asciidoctor PDF]] and the [[DocBook]] toolchain support creating an index catalog automatically. The built-in HTML5 converter in Asciidoctor does not generate an index.

Define a level 1 section `==` marked with the style `index` at the end of your document.

In a multipart book, the index can be the last level 0 section `=`.

```
[index]
== Index
```