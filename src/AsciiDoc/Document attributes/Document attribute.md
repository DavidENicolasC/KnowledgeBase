Each document holds [[Attribute]]s, called together document attributes. Provide a means of configuring the [[AsciiDoc Processor]], declaring [[Document metadata]], and defining reusable content.

AsciiDoc defines a set of built-in attributes, and also allows the author (or extension) define additional document attributes, which may replace built-in attributes when permitted.

The attribute is available from the point it is set until it is unset.

Attributes defined in the body are not available via the document metadata.

Unless blocked, it can be unset or assigned a new value in the document header or body.

Can also be declared (set with an optional value or unset) outside the docu­ ment via the CLI and API. [[Attribute Entry]] syntax is not used in these cases.

There are types:
- [[Built-in attribute]]s
- [[User-defined attribute]]s