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
