 Are automatically retained in [[Literal Block]]s, [[Listing Block]]s, [[Source Block]]s, [[Verse Block]]s and [[Paragraph]]s.
 
For any single line, you can terminate it with a space followed by a plus sign.
```
line one +
line two
```

To add this behavior to every line in the paragraph, set the `hardbreaks` option on the paragraph instead.
```
[%hardbreaks]
line one
line two
```

Alternatively, you can set the [[hardbreaks-option Document Attribute]]
```
:hardbreaks-option:

line one
line two
```