you can nest a [[Component]] into another component. Here, MyButton is the nested component:
```
export default function MyApp() {
	return (
		<div>
			<h1>Welcome to my app</h1>
			<MyButton />
		</div>
	);
}
```