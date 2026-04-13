Used for assign attributes to [[Block]] and [[Inline element]]s. Referred as `attrlist`.

```
first-positional,second-positional,named="value of named"
```

Entries are separated by `,`, excludding commas inside quotes.

For [[Block]]s, is placed inside one or more [[Block attribute line]]s.

For [[Block macro]]s and [[In-line macro]]s, is placed between the square brackets of the macro. The text in a block macro **never** needs to be escaped. For an inline macro, it may be necessary to escape the text to avoid prematurely ending the [[Macro]] or unwanted substitutions.

```
name::target[first-positional,second-positional,named="value of named"] 
```

For [[Formatted Text]], is placed in the square brackets in front of the text enclosure. However, formatted text only supports a restricted form of the attribute list. Specifically, it does not support named attributes, only the attribute shorthand syntax.

```
[#idname.rolename]*text with id and role*
```

The schema is [[open-ended]]. Any posi­ tional or named attributes that are not recognized will be stored on the element, but will not have an impact on the behavior or output.