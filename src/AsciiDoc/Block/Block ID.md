You can assign an ID to any block using an [[Block attribute list]].

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

All other block attributes above are typically separated by commas `,`, except when [[`role`]] and [[`options`]] attributs are assigned values using their shorthand syntax (`.` and `%`).