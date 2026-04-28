[[JSX]] lets you put markup into JavaScript. Curly braces let you “escape back” into JavaScript so that you can embed some variable from your code and display it to the user.

```
return (
	<h1>
		{user.name}
	</h1>
);
```

You can also “escape into JavaScript” from JSX attributes, but you have to use curly braces _instead of_ quotes.

```
const user = {
  name: 'Hedy Lamarr',
  imageUrl: 'https://react.dev/images/docs/scientists/yXOvdOSs.jpg',
  imageSize: 90,
};

export default function Profile() {
  return (
    <>
      <h1>{user.name}</h1>
      <img
        className="avatar"
        src={user.imageUrl}
        alt={'Photo of ' + user.name}
      />
    </>
  );
}
```