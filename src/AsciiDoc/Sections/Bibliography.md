Must be its own [[Section]] at any level.

You would define the bibliography as a level 1 section `==` when:
* The doctype is [[article Document Type]]
- The doctype is [[book Document Type]] and the book doesn’t contain any [[Book Part]]s
- Is for a [[Book Part]].
```
[bibliography]
== Bibliography
```

When defining as a deeper section, doctype doesn´t matter and it’s scoped to the [[Parent Section]].

If the [[book Document Type]] has [[Book Part]]s, and the bibliography is for the whole book, the section is defined as a 0 [[Section Level]] `=`.
```
[bibliography]
= Bibliography
```

Are declared as [[Item]]s in an [[Unordered List]]

For reference it, you need to assign a _non-numeric_ label to the entry. To assign this label, prefix the entry as a [[Bibliography Anchor]]. You can reference  the entry from anywhere above the bibliography in the same document using the [[Normal Cross Reference]].

 Both converted to `[<label>]`, where `<label>` is the ID of the entry. If specify [[xreftext]] on the [[Bibliography Anchor]] (e.g. `[[[label,xreftext]]]`), converts to `[<xreftext>]` instead.

If want both appears as a number, assign the number to the entry by using the [[xreftext]].
 `[[[label,1]]]` will be converted to `[1]`.