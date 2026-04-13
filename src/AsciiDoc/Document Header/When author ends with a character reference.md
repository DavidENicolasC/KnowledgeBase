You must escape it from processing. One way to escape it is to add a trailing [[Attribute Reference]].
```
{empty}
```

Like in this

```
AsciiDoc&#174;{empty} WG; Another Author
```

You can also move the character reference to an [[Attribute]] and use an [[Attribute Reference]]:
```
:reg: &#174;
AsciiDoc{reg} WG; Another Author
```

Important: Segments of the [[author Attribute]] will not be processed.