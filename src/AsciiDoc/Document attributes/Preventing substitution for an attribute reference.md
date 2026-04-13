- Prefix the element with a backslash (`\`). If text into that follows the backslash does not match an [[Attribute Reference]], the backslash will not be removed during processing.

```
\{name-of-attribute}
```

- Enclose it in an [[Inline Passthrough]]. In this case, the processor uses the normal substitution rules for the passthrough type you have chosen. You don’t have to worry whether the curly braces form an attribute reference or not. All the text between the passthrough enclosure will get passed through to the output. 

```
In the path +/items/{id}+, id is a path parameter.
```

