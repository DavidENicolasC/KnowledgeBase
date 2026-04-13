Is a [[Named Attribute]].

For assign, you can use two syntaxes:

Shorthand syntax (`%`):
```
[%option]
****
This is a sidebar with an option assigned to it, named option.
**** 
```

Shorthand syntax for multiple values:
```
[%option1%option2]
****
This is a sidebar with two options assigned to it, named option1 and option2.
**** 
```

Formal syntax (use either `opts` or `options`):
```
[opts=option]
****
This is a sidebar with an option assigned to it, named option.
****
```

Formal syntax for multiple values:
```
[opts="option1,option2"]
****
This is a sidebar with two options assigned to it, option1 and option2.
****
```