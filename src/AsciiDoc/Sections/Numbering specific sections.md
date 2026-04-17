Insert the attribute above the section where you want [[Numbering Sections]] to cease and unset it by adding an exclamation point to the end of its name.

```
= Title
:sectnums:

== Numbered Section

:sectnums!:

== Unnumbered Section

== Unnumbered Section

=== Unnumbered Section

:sectnums:

== Numbered Section
```

To turn section numbering back on midstream, reset the attribute above the section where numbering should resume.

For regions of the document where section numbering is turned off, the section numbering will not be incremented.