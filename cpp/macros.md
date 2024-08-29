# Macros
A rule that defines how input text is converted to output text.
Uses a `#define` directive. There are two types: function-like and object-like. Avoid function-like macros.

## Object-Like Macros
These have two subtypes: with and without substitution text.
`#define IDENTIFIER
#define IDENTIFIER substitution_text`

Object-like macros with substitution text are a legacy feature from C, and should be avoided.
Without substitution text is okay, and they are often uses for things like conditional compilation.
