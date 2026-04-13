The primary mechanism for defining a [[Document Attribute]] in an AsciiDoc document.

You can think of it as a global variable assignment for AsciiDoc.

Becomes available from the point where declared to forward in the document.

Fre­quently used to toggle features.

Must be entered of its own line.

Consists of two parts:
- Attribute **name** - Comes first
- Attribute **value** - Optional, comes next, offset by at least one space.

```
:attribute-name: optional attribute value
```

You can reference other attributes - is resolved inmediately

```
:url-org: https://example.org/projects
:url-project: {url-org}/project-name
```

There are types:
- [[Header attribute]]
- 