An attribute reference can be used to set or unset this.

Allows you to set or unset an attribute in places where [[Attribute Entry]]s lines are not permitted, such as in a normal table cell or a list item.

```
{set:name:value}
```

Value segment is optional. Value defaults to empty string.

```
{set:name} OR {set:name!}
```

Are processed when attribute references are replaced, as part of the attributes substitution.

Therefore, the result of the assignment is only available to attribute references that follow it.

These assignments are not visible in the document model after the document has been loaded. 