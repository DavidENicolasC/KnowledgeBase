set [[sectnums Attribute]] ([[Numbering sections]]) and assign it a value of `all`.

```
= Title
:sectnums: all 
```

Assignment of [[Appendix Number]]s isn’t affected by [[sectnums Attribute]] as their section title prefixes are controlled by the [[appendix-caption Attribute]].

[[book Document Type]] parts aren’t numbered by sectnums either, instead, they’re controlled by [[partnums Attribute]].