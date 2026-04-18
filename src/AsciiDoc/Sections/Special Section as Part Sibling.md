Apply for cases where you want the special section to be owned by the [[book Document Type]] instead, as a sibling of [[Book Part]]s.
```
= Multi-Part Book
:doctype: book

= Part Title

== Chapter Title

[appendix]
= Appendix Title
```

If supports nested sections, the next level must be level 2 `===`, since the special section itself has level 1.
```
= The First Part

== The First Chapter

Chapters can be grouped by preceding them with a level 0 Book Part title.

[appendix]
= The Appendix

=== Basics

A multipart book can have appendixes, which should be defined at section level 0.

=== Subsections

Subsections of an appendix in a multipart book should start at level 2.
```