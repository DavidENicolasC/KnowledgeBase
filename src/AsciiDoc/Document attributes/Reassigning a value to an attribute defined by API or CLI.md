Add the `@` precedence modifier to the end of the [[Attribute Value]] or the end of the [[Attribute Name]].

Can be named "soft-setting".

```
$ asciidoctor -a imagesdir=images@ doc.adoc


$ asciidoctor -a imagesdir@=images doc.adoc
```

You can then override the value:
```
= Document Title :imagesdir: new/path/to/images
```

You can soft unset an attribute:
```
!name=@
```