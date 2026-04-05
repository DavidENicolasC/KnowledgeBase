Consider the following example:
```
[listing]
....
a > b
....
```

Since declared [[src/AsciiDoc/Block/Block style|Block style]] (the first positional [[Attribute]] of the [[Block attribute list]]) matches the name of a [[Context]], Context becomes declared block style and resolved block style remains unset. That is, resolved block style differs from declared block style.

When change a block context using the declared block style block retains the simplest content model. When masquerading the context of a [[Structural containers]], only contexts preserving the expected content model are permitted.

If [[Block style]] matches the name of a [[Context]], sets the block context to that value and resolved block style will be left unset. If does not match a context name, it will either specialize the context and optionally set the context implicitly.