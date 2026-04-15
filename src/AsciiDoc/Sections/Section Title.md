Must be prefixed with a [[Section Marker]], which indicates the [[Section Level]].

Can only have a single primary ID.

It’s possible to register [[Auxiliary ID]]s for referencing from the URL using [[Inline Anchor]]s.

Is interpreted as [[Paragraph Text]] if it’s found inside of a nonsection [[Block]] unless it marked as a [[Discrete Heading]].

```
= Document Title (Level 0)

== Level 1 Section Title

=== Level 2 Section Title

==== Level 3 Section Title

===== Level 4 Section Title

====== Level 5 Section Title

== Another Level 1 Section Title
```

In the HTML output, is represented by a [[Heading Tag]]. The number of the heading tag is one more than the section level (e.g., section level 1 becomes an `h2` tag).