# GCD, LCM, Primallity, and RSA
## Concepts and Definitions
Fundamental Theorem of Arithmetic: every positive int >= 1 can be expressed uniquely as a product of primes where the primes are written in non-decreasing order (non-decreasing means all to the right are bigger than OR EQUAL TO all to the left).
Multiplicities: occurences of factors => 120 = 2 \* 2 \* 2 \* 3 \* 5 = 2^3 \* 3 \* 5
Relative Primality (aka coprime): Two integers whose GCD is 1
Small Factors Theorem: if N is composite, then N has a factor > 1 and at MOST sqrt(N).
- Used to optimize brute force prime factoring.

Prime Number Theorem: a random number between 2 and N has a 1/ln(N) likelihood of being prime
- Density of primes between 2 and N is N/lnN

GCD Theorem: let x and y be ints > 0. Then, GCD(x,y) = GCD(y mod x, x)
- Since y mod x = x, you can use y mod x as a smaller, more manageable number

## GCD and LCM Algos
1. Get prime factorization of both integers
2. Create set with both integers' primes (put a 0 for factors that appear in one's primes but not another)
3. GCD is product of primes with min exponents
4. LCM is product of primes with max exponents

## Prime Division
1. Take the prime factorization and focus on commonn factors
2. Subtract exponents
3. Multiply what is left

## Euclidean Algo
Finds the GCD quickly
```python
def euclidean_algo(x, y):
    if x > y:
        x, y = y, x
    
    r = y % x # % is mod
    while r != 0:
        y = x
        x = r
        r = y % x
    return x
```
The number before the result of 0 is the GCD.

## Extended Euclidean Algo
Finds GCD as a linear combination of x and y
GCD(x, y) = sx + tn

You do the EA and then sub all equations in to get the linear combo

## Multiplicative Inverse & EEA
Normal inverse is reciprocal, but not in modular arithmetic

### Multiplicative Inverse mod n
Inverse mod n of an integer x, is an int s in Zsubn such that sx mod n = 1
- **Not every number has an inverse mod n**

#### Using EEA to Find Multiplicative Inverse:
s mod n

## Fast Exponentiation
Convert exponent to binary expansion, then multiply x^b^a, x^b^a-1... (index the exponents by 0) then drop any that are 0. Multiply together and you get the result

## Modular Exponentiation
Successive Squaring

## Encryption
Cannot have collisions, and encryption scheme is inverse of decryption

## RSA
### Key Generation
1. Select two large primes, p and q
2. Calculate N, phi, e, and d
- N = p \* q
- phi = (p - 1) \* (q - 1)
- e = GCD(e, phi)
- d = multiplicative inverse of e mod phi
3. d is private key, N and e are public

### Encryption in RSA
m = c^d mod N
- May need to break up value of m if it is over N and concatenate the encrypted blocks

### Decryption in RSA
c = m^e mod N
==Use mod_exp function! The args are a = m, b = e, c = N==

