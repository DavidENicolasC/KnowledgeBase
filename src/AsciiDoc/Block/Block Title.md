Is defined in its own line directly above the [[Block attribute list]], [[Structural containers]] or [[Block]] content. The line must begin with a dot `.` and immediately be followed by the text of the title (without spaces). Must only occupy a single line a thus cannot be wrapped.

```
.This a block title above a delimited block. Is displayed out of the container, an padded to left.
****
This is the block content.
****

.This is another block title above a declared block style
[source, yaml]
----
image: node:16-buster
stages: [ init, verify, deploy ]
----

.This is another title above a non-delimited block (Will be centered and displayed into the container).
Mint has visions of global conquest. If you don´t plant it in a container, it will take over your garden.
```

Should not be confused with an [[Ordered list item]] that uses the same `.` marker. The block title has no space after the `.`, whereas the space after a list marker is required.

There are types:
- [[Captioned title]]