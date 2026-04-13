Are declared using the `:attributes` option (which supports various entry formats).

The assigned value is stored as is, meaning substitutions are not applied to it.

Subsequent substitutions, such as the macro substitution, do get applied.

Are implicitly a document header attribute, and becomes locked unless you add an `@` to the end of the attribute name or value.

Exception is [[sectnums]] attribute.