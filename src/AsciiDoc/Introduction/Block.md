Lay down the document structure in an [[AsciiDoc Document]]. May contain other blocks. Can have [[Block metadata]]. Should always be bounded by an empty line or [[Document boundary]] on either side. Each block contains a [[Content model]], which can be determined by circunstances ([[Context]] and [[Block Style]]). Have a [[Context]].

Are defined using some form of [[Line]]-oriented syntax. [[Section block]]s begin with a [[Section title]] line. [[Delimited block]]s are enclosed in a matching pair of delimiter lines. [[Paragraph block]]s must be contiguous lines.

All acommodate zero or more lines of metadata stacked linewise directly on top of the block. These populates [[Block properties]].

Its identity is defined by the [[Context]] and the [[Block Style]].

There are types:
* [[Paragraph block]]
* [[Section block]]
* [[Verbatim block]]
* [[Compound block]]
* [[Delimited block]]

Paragraph blocks and verbatim blocks have an implicit and modifiable set of [[Substitution]]s. This do not apply to Compound blocks.

Can have multiple [[Role Attribute]]s and options.