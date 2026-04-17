Contains factual information about the book, particularly relating to its production. It may include information such as the [[ISBN]], publishing house, edition and copyright dates, legal notices and disclaimers, typographic style, fonts and paper used, cover art and layout credits, bind­ ing method, and any other significant production notes.

Almost always occur at the very beginning (front matter) or end (back matter) of a book.

Can also be placed anywhere in an AsciiDoc manuscript as a top-level section.

In a printed book, the colophon is often found on the verso side of the [[Title page]].

For use it, document type must be a [[book Document Type]].

If does not have parts, must be a level 1 section `==` ([[Section Level]]).

```
[colophon]
== Colophon

The Asciidoctor Press, Ceres and Denver.

(C) 2020 by The Asciidoctor Press

Published in the Milky Way Galaxy.

This book is designed by Dagger Flush, Denver, Colorado.
The types are handset Volcano Dust and Papaya, designed by Leeloo.
Leeloo created the typefaces to soften the bluntness of documentation.

Built with Asciidoctor on Fedora 33.

Printing and binding by Ceres Lithographing, Inc., Ceres, Milky Way. 
```

If have parts, must be a level 0 section `=`.

```
[colophon]
= Colophon The Asciidoctor Press, Ceres and Denver.

(C) 2020 by The Asciidoctor Press Published in the Milky Way Galaxy.

This book is designed by Dagger Flush, Denver, Colorado.
The types are handset Volcano Dust and Papaya, designed by Leeloo.
Leeloo created the typefaces to soften the bluntness of documentation.
```

Only be numbered when [[Numbering special sections]].