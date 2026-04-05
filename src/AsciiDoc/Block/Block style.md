When specified, is the declared block style. Is the first positional (unnamed) [[Attribute]] in the in the [[Block attribute list]]. Is the value the author supplies. Is then interpreted and resolved. This resolved block style specializes the block's context.

Can be used to change [[Context]] of a [[Block]]. This is referred to as [[Block masquerading]].

```[asciidoc]
[source,ruby]
----
puts "Hello, World!"
----
```

Above, context of a source block is [[listing]] and style is [[source]]. The [[Style]] specializes the block as a source block.

The resolved block style specializes the [[Context]] to give it special behavior or semantics, or can also be used to change the context itself.