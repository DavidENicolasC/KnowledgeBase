Set the `notitle` option (e.g., `%notitle` or `opts=notitle`) (previously `untitled`) on the section.

```
[dedication%notitle]
== Dedication

For S.S.T.--

thank you for the plague of archetypes.
```

Although the title is hidden in the output document, it still needs to be specified in the AsciiDoc source for the purpose of referencing. The title will be used as the [[reftext Attribute]] of a cross reference, just as with any section.