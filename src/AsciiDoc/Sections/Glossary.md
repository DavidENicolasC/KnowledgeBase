Set the `glossary` [[Block Style]] on a [[Section]].

Defined as a level 1 section (`==`) when:
- The doctype is [[article Document Type]]
- The doctype is [[book Document Type]] and the book doesn’t contain any [[Book Part]]s
- Is for a [[Book Part]]
```
[glossary]
== Terminology
```

When the glossary is for the whole [[book Document Type]] and has parts, the section is defined as a level 0 section `=`.
```
[glossary]
= Glossary
```

The block style `glossary` must be set on the description list in the section too.
```
[glossary]
== Glossary

[glossary]
mud:: wet, cold dirt
rain::
	water falling from the sky
```