Only primary ID in [[Section Title]] can be used for referencing the section title within the document.

```
== [[secondary-id]][[tertiary-id]]Section Title

[#primary-id]
== [[secondary-id]][[tertiary-id]]Section Title

== Section Title[[secondary-id]][[tertiary-id]]
```

Where you place the [[Inline anchor]] is where it will end up in the output.

Are not registered with the [[Referencing System]]. That means they cannot be used for referencing the [[Section Title]] within the [[AsciiDoc Document]].

Only intended for assigning auxiliary fragment identifiers to the section title so it can be referenced the from the URL using a URL fragment (aka deep linking).