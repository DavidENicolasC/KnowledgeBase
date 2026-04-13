Only consist of a value.

Position is the 1-based index of the entry once all named attributes have been removed (so they may be interspersed).

May be dually assigned to an implicit attribute name if the block or macro defines a mapping for it.

```
icon: 1 ⇒ size
image: and image:: 1 ⇒ alt (text), 2 ⇒ width, 3 ⇒ height
Delimited blocks: 1 ⇒ block style and attribute shorthand
Other inline quoted text: 1 ⇒ attribute shorthand
link: and xref: 1 ⇒ text 
```

Custom blocks and macros can also specify it.

The following sentences attribute lists are equivalents.
```
image::sunset.jpg[Sunset,300,400] image::sunset.jpg[alt=Sunset,width=300,height=400] 
```