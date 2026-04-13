Is a [[Named Attribute]].

Adds additional semantics to an element.

Can be used to apply additional styling to a group of elements (e.g., via a [[CSS]] [[Class Selector]])

May activate additional behavior if recognized by the [[Converter]].

Always mapped to the `class` attribute in HTML ouput.

You can assign roles either by:

Shorthand syntax
```
[.rolename]
**** This is a sidebar with a role assigned to it, rolename. ****
```

Shorthand syntax for multiple roles. Use space ` ` for separate roles.
```
[.role1.role2]
**** This is a sidebar with two roles assigned to it, role1 and role2. 
```

Formal syntax ([[Named Attribute]]). Cannot be used for [[Formatted Text]]:
```
[role=rolename]
**** This is a sidebar with one role assigned to it, rolename. **** 
```

For multiple roles. Quotes not strictly required:
```
[role="role1 role2"]
**** This is a sidebar with two roles assigned to it, role1 and role2. **** 
```