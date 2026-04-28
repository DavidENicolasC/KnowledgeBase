In [[React apps]], you specify a CSS class with `className`.

React does not prescribe how you add CSS files. In the simplest case, you’ll add a `<link>` tag to your HTML.

Works the same way as the [[HTML class attribute]]:

```
<img className="avatar" />
```

Then you write the CSS rules for it in a separate CSS file:

```
/* In your CSS */
.avatar {
border-radius: 50%;
}
```

You can use the `style` attribute when your styles depend on JavaScript variables.
```
  return (
    <>
      <h1>{user.name}</h1>
      <img
        className="avatar"
        style={{
          width: user.imageSize,
          height: user.imageSize
        }}
      />
    </>
  );
}
```