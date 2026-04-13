You can use it by API.

```
title_parts = document.doctitle partition: true
puts title_parts.title
puts title_parts.subtitle
```

You can also partition in an arbitrary way by passing the separator.

```
title_parts = document.doctitle partition: '::'
puts title_parts.title
puts title_parts.subtitle
```