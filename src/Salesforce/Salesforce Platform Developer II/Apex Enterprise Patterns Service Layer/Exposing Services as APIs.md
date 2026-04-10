Change modifiers from `public` to `global`

However, it has implications when changing method signatures between AppExchange package releases:
- You can’t add an abstract method to a global class after the class has been uploaded in a Managed - Released package version.
- You can’t override a public or protected virtual method of a global class of an installed managed package.