Lay down the document structure in an [[AsciiDoc Document]]. May contain other blocks. Can have [[Block metadata]]. Should always be bounded by an empty line or [[Document boundary]] on either side. Each block contains a [[Content model]], which can be determined by circunstances ([[Context]] and [[Block style]]). Have a [[Context]].

Are defined using some form of [[Line]]-oriented syntax. [[Section block]]s begin with a [[Section title]] line. [[Delimited block]]s are enclosed in a matching pair of delimiter lines. [[Paragraph block]]s must be contiguous lines.

All acommodate zero or more lines of metadata stacked linewise directly on top of the block. These populates [[Block properties]].

There are types:
* [[Paragraph block]]
* [[Section block]]