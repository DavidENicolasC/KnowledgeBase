You can enclose the value in the [[Inline Pass Macro]].

```
:app-name: pass:quotes[MyApp^2^]


OR


:app-name: pass:q[MyApp^2^]

```

This is done by manipulating the substitutions applied to the text where it is referenced.

```
:app-name: MyApp^2^

[subs="specialchars,attributes,quotes,replacements,macros,post_replacements"] The application is called {app-name}. 
```