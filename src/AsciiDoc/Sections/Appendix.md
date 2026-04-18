 Can be used in [[book Document Type]] and [[article Document Type]], and it can have sub[[Section]]s.

 Must be defined as a 1 [[Section Level]] `==` for articles. For books, can be either 1 or 0 section level, as you could want to be it adjacent to other parts in a [[Multi-part Book]].

 First subsection of the appendix must be a level 2 section `===`.

Have an [[Appendix Label]].
```
= Article Title
:appendix-caption: Exhibit
:sectnums:
:toc:

== Section

=== Subsection

[appendix]
== First Appendix

=== First Subsection

=== Second Subsection

[appendix]
== Second Appendix

[appendix]
= Third Appendix

=== First Subsection

=== Second Subsection
```