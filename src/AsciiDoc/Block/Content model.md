Determines what kind of content the block can have and how is processed. Also determines if the block can be nested. Can be inferred by for all built-in syntax, but can be configured.

There are types:
- **Compound** - Block that may only contain other [[Block]]
- **Simple** - Block that´s treated as contiguous lines of paragraph text, as a [[Paragraph block]].
- **Verbatim** - Block that holds [[Verbatim text]]
- **Raw** - Holds unprocessed content passed directly through the output with no substitutions applied.
- **Empty** - Has no content
- **Table** - Special content model reserved for tables that enforces a fixed structure.