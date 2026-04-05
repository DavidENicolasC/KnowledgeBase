Title prefixed with a caption label and a number followed by a dot.

```
Table 1. Properties
```

Only displayed when the corresponding caption attribute is set in the [[Block style]].

Blocks supporting captioned titles

| Block [[Context]] | Caption attribute | Counter attribute |
| ----------------- | ----------------- | ----------------- |
| appendix          | appendix-caption  | appendix-number   |
| example           | example-caption   | example-number    |
| image             | figure-caption    | figure-number     |
| listing, source   | listing-caption   | listing-number    |
| table             | table-caption     | table-number      |

All caption attributes are set by default except for `listing-caption`. The number is sequential, computed automatically, and stored in a corresponding counter attribute.

[[Delimited block]] supporting captioned title by default
```
.Block supporting captioned title
====
Block content
====
```

We can set the start number or the next number selected in sequence for the counter attribute.

We can also customize the caption, including if the counter should start with a letter.
```
.Block title
[caption="Example {counter:my-example-number:A}: "]
====
Block content
====
```

This will be displayed as:
```
Example A: Block Title
```