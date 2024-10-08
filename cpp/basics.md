# C++ Basics
## iostream
Relevant operators:
- extraction operator: `std::cin >> x;`
- insertion operator: `std::cout << "hello" << "world!\n";`

### std::cin (character in)
This is the standard way to receive user input, and accepts input until you press `enter`.
It stores the input in a memory buffer delimited by `\n`. The extraction operator gets the next item from the std::cin buffer.
`int x;
std::cout << "Enter an integer: ";
std::cin >> x;`

### std:cout (character out)
This lets you print data to stdout. It is buffered as well, and you can add multiple things to the buffer with the insertion operator.
`std::cout << "hello" << "world!\n";`

#### std::endl vs '\n'
`std::endl` manually flushes the buffer, which is costly, while `\n` does not. Prefer `\n`.

## Variables
An object is a region of memory (not including functions) and has nothing to do with OOP. A named object (as opposed to a anonymous
object) is a variable. A temporary is an unnamed/anonymous object created by the compiler to temporarily store a value.

### Initialization
- Uninitialized: object does not have a value yet
- Initialized: object given known value at point of definition
- Assignment: object given known value beyond point of definition

*Best Practice*: always initialize variables.

#### Initialization Methods
There are a lot, but direct list initialization (aka "uniform initialization") is preferred: `int x {5};`
- This also prevents narrowing.

#### Default vs Value Initialization
Default: `int x;` has undetermined value
Value: `int x {};` initialized as empty

*Best Practice*: Don't use default initialization. Use `{0}` if you want it to be zero, and `{}` if you want it to be a temporary.

## Operators
Besides the basic operators, C++ has a few more (see iostream section for extraction and insertion).
Operators have an arity, or the number of operands it takes.
- Unary
- Binary
- Ternary
- Nullary (only throws)

Symbol operators like `+` are often referred to as "operator\<symbol\>".

## Bad Behavior
Undefined Behavior is the result of code not well-understood by the C++ language.
Implementation-Defined Behavior is not defined by the C++ standard, but is compiler-specific and well-documented.
Unspecified Behavior is like Implementation-Defined Behavior but is not required to be documented.

*Best Practice*: Avoid using any of the above.
