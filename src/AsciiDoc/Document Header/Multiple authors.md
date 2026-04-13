Their [[Built-in attribute]] reference is the same as in [[author Attribute]], and adding a `_<n>` number, where `n` is the `1-based` index. Index `1` is optional.

```
.About {author_2}
Mr. {lastname_2} lives in the Rocky Mountains.

.About {author_3}
{firstname_3}, also known as {authorinitials_3}, loves to surf.

.About {author}
You can contact {firstname} at {email}.
```

The rules for it is the same that the original attributes in [[author Attribute]].

Each author is concluded with a semicolon `;`.
```
Kismet R. Lee <kismet@asciidoctor.org>; B. Steppenwolf; Pax Draeke
```

Only HTML5 and DocBook can convert this.

You can only use [[Author Line]] for this. You can not use [[author Attribute entries]].