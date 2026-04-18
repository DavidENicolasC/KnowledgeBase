Can only be used when the [[Document Type]] is [[book Document Type]].

Presence implies that the document is a [[Multi-part Book.]]

Is a level 0 section. ([[Section Level]])

Must contain a at least one level 1 section.

First part is the first level 0 section in the document that comes after the [[Document Title]].

Is designated by a level 0 section title `=`.

```
= Book Title
:doctype: book

= Part I
```

Can have an optional introduction known as a [[Part Intro]].

Can have its own [[Preface]], [[Bibliography]], [[Glossary]] and [[Index]].

```
= Multi-Part Book with Parts that Have Special Sections
Author Name <author@example.com>
:doctype: book

[preface]
= Book Preface

This is the preface for the whole book.

=== Preface Subsection

Chinchillas rule the world.

= Part 1

This is the introduction to the first part of our mud-encrusted journey.

== Chapter 1

There was mud...

== Chapter 2

Great gobs of mud...

[glossary]
== Part 1 Glossary

[glossary]
mud:: wet, cold dirt

= Part 2

[preface]
== Part 2 Preface

This is a preface just for part 2.

== Chapter 3

The mud had turned to cement... 
```