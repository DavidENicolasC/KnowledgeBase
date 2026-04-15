[[AsciiDoc Processor]] will automatically generate and assign an [[Block ID]] for the block using the title or [[Section Title]].

It begins the value with an underscore `_` and uses a hyphen `_` between each word.
```
_wiley_sons_inc
```

This ID is generated as follows:

1. Inline formatting is applied (in title substitution order)
2. All characters are converted to lowercase.
3. The value of the [[idprefix Attribute]] (`_` by default) is prepended.
4. Character references, HTML/XML tags (not their contents), and non-word characters (except for space, hyphen, and period) are removed.
5. Spaces, hyphens, and periods are replaced with the value of the [[idseparator Attribute]] (`_` by default)
6. Repeating separator characters are condensed.
7. If necessary, a sequence number is appended until the ID is unique within the document.

Can be expected to be safe to use in an HTML document. However, does not necessarily conform to an [[NT-Name]], as required by the [[XML specification]].

When producing DocBook, and [[Section Title]] uses not permitted word characters in an [[XML ID]], you must either provide an explicit ID that is conforming, or encode those invalid ID characters using a character reference (e.g., `&#x2161;`).