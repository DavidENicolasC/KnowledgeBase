Encapsulates the [[Document Title]], [[Author]] and [[Revision Information]], [[Document-Wide Attribute]]s, and other [[Document Metadata]].

No content [[Block]]s are permitted above it.

The document header may not contain empty lines. First empty line that the [[AsciiDoc Processor]] encounters after this marks the end and the start of the [[Document Body]].

Can contain:
- Optional [[Document Title]] (a level-0 heading)
- Optional [[Author Line]] or author and [[Revision Line]]s if the document title is present (should imme­diately follow the document title)
- Optional [[Document-Wide Attribute]]s (built-in and user-defined) declared using attribute entries
	- Includes [[Optional Metadata]], such as a description or keywords
- Optional [[Comment Line]]s.

Only required for [[manpage Document Type]].

You would see the following warning for [[article Document Type]] when put content blocks above this:
```
level 0 sections can only be used when doctype is book
```