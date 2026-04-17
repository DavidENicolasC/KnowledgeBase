level 1 `==` through level 3 `====` section titles are numbered by default.

You can increase or reduce the section level limit by setting the sectnumlevels attribute and assigning it the section level up you want it to number.

Accepts a value of 0 through 5, and it can only be set in the document header.

```
= Title
:sectnums:
:sectnumlevels: 2
```

When set to `2`, levels 3 to 5 are not numbered.

When set to `0`, is effectively the same as [[Disabling section numbering]].