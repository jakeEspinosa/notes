# Modular Arithmetic
## Concepts
Modular = cyclical, like a 12-hour clock. Only deals with integers
x|y == x divides y
x div y == x integer-divided by y (only integer results)
x mod y == x modulus-divided by y (only integer remainder)
You perform the arithmetic/multiplication, then apply modulo.

## Notation
Z == set of all ints
ZsubN == set of all ints in modular addition, subtraction, and mod (remember it is cyclical)

## Division Algo
Let x, y, and z be ints. If x|y and x|z, then x|(sy + tz) for any ints t and z.

### Negative Division
Divide, make divisor one up from decimal divisor, then whatever you need to add to the negative dividend is the remainder.

### Positive Division
Find the closest that doesn't bust, then add the remainder.

## Congruence Modulo n
x is congruent to y mod n if x mod n = y mod n (denoted with three horizontal lines).
- Alternatively, x = y mod n if and only if n|(x-y)

## Exponentiation
(43^17 + 32 \* 139) mod 7 = [(43 mod 7)^17 + (32 mod 7) \* (139 mod 7)] = (1 + 24) mod 7 = 4
- **You gotta convert THEN compute**
