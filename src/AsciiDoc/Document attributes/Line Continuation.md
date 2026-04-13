Consists of a space followed by a backslash character (\) at the end of the line.

Must be placed on every line of a multiline value except for the last line.

```
:description:If you have a very long line of text \
that you need to substitute regularly in a document, \
you may find it easier to split the value neatly in the header \
so it remains readable to folks looking at the AsciiDoc source. 
```

When line continuation character missing, [[AsciiDoc Processor]] will assume it has found the end of the value and will not include subsequent lines in the value of the attribute.