Controls how missing references are handled. 

By default, missing references are left behind so the integrity of the document is preserved and it’s easy for the author to track down.


Has four possible values:

- **skip** - Leave the reference in place (default setting) - ex. `Hello, {name}!`
- **drop** - Drop the reference, but not the line - ex. `Hello, !`
- **drop-line** - Drop the line on which the reference occurs (matches behavior of AsciiDoc.py) - ex. ``
- **warn** - print a warning about the missing attribute - ex. `asciidoctor: WARNING: skipping reference to missing attribute: XYZ `