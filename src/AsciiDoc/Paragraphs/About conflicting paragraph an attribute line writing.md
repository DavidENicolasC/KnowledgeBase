First line from a [[Paragraph]] cannot start with `[` and end with `]`, cause will be treated as [[Block Metadata]], specifically a [[Block Attribute Line]].

There are two ways to work around this issue. First, you can add any text in front of the `[` that will otherwise not be rendered to disrupt the syntax match. For example, you can start the paragraph with the attribute reference `{empty}`.
```
{empty}[.rolename]*main text*footnote:[The footnote.]
```
Another way to solve the problem is to write the paragraph as a literal paragraph, then override the implicit style using the explicit [[Normal Style]].