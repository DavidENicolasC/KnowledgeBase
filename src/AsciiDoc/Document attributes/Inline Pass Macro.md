Their syntax is `pass:[]`.

Accepts a list of zero or more substitutions in the target slot, which can be used to control which substitutions are applied to the value. If no substitutions are specified, no substitutions will be applied.

It must completely surround the attribute value. If it’s used anywhere else in the value, it will be ignored.

If the processor detects that an inline pass macro completely surrounds the attribute value, it:

- Reads the list of substitutions from the target slot of the macro 2
- Unwraps the value from the macro 3
- Applies the substitutions to the value