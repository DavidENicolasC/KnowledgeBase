Any inline formatting in an attribute value isn’t interpreted because:

- Inline formatting is not applied when the AsciiDoc processor sets an attribute
- Inline formatting is not applied when an attribute is referenced since the relevant substitutions come before attributes are resolved.