- [[Declare document attribute from API]]
- [[Declare document attribute from CLI]]

Substitutions are not applied.

If the value contains XML special characters, that means those characters must be pre-escaped. The exception would be if you intend for XML/HTML tags in the value to be preserved. If the value needs to reference other attributes, those values must be pre-replaced.

```
$ asciidoctor -a equipment="a bat &amp; ball" document.adoc


To play, you'll need {equipment}.
```