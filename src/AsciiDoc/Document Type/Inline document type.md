For when you only want to apply inline [[AsciiDoc]] formatting to input text with­out wrapping it in a [[Block]] element.

Rules:
- Only a single [[Paragraph]] is read from the AsciiDoc source
- Inline formatting is applied
- The output is not wrapped in the normal paragraph tags.

Given:

```
https://asciidoctor.org[AsciiDoc] is a _lightweight_ markup language...
```

Processing with `doctype=inline` and `backend=html5` produces:
```
<a href="https://asciidoctor.org">AsciiDoc</a> is a <em>lightweight</em> markup language&#8230;
```