Its purpose is to identify the element when linking, scripting, or styling. Thus, the identifier can only be used once in a document.

Can be used for adding additional styling to specific elements (e.g., via a CSS ID selector)

You can assign an ID to any block using an [[Attribute List]].

You can use the shorhand syntax `#`. Only requires that the id is not empty.

```
[#this-is-an-id]
====
Content of the delimited example block.
====

[quote#id-attached-to-a-declared-style-attribute]
Roads? Where we're going, we don´t need roads.

[quote#id-attached,positional Attribute]
Dummy text
```

You can also use the following syntaxes:
- Longhand - `id=` - Spaces are not permitted.
```
[id=goals]
* Goal 1
* Goal 2
```
- Anchor - `[[]]` - Spaces are not permitted.
```
[[goals]]
* Goal 1
* Goal 2
```

All other block attributes above are typically separated by commas `,`, except when [[`role`]] and [[`options`]] attributs are assigned values using their shorthand syntax (`.` and `%`).

Is a [[Named Attribute]].

It's recommended to use the [[Standard for Block IDs]].