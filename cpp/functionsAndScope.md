# Functions and Files
## Functions
### Parameters
- Unreferenced Param: named params that are not used.
- Unnamed Param: param not used or named.

*Best Practice*: use unnamed params, not unreferenced params, and put the name in a comment.

## Defintions and Declarations
Declaration: tells the compiler about the existance of an object. `int x;`.
Definition: implements/instantiates the identifier. `int x {42};`
All definitions are declarations, but not all declarations are definitions (called a pure declaration).

### Forward Declarations
Tells the compiler about the existance of an identifier before defining it.
`int add(int x, int y);`.

## Scope
### Namespaces
Can only contain definitions and declarations, not executable statements.
Uses `::` to resolve scope: `std::cout`.
- If nothing is on the left of the scope resolution operator, it is assumed to be `std`.

You should avoid `using` directives, as they defeat the entire point of namespaces.
