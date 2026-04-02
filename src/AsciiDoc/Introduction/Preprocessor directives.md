Function that controls [[Line]]s that are fed to the parser. Must be on a line itself. Can access [[Document attributes]]. Can have [[Element attributes]] that only apply to the preprocessing operation itself.

There are two types:
- Conditional directive - Configure lines to be included or excluded based on the presence of an attribute, or arbitrary condition.
- Include directive - Add additional lines to the document taken from another document.