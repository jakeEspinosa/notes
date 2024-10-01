# Base b Expansion
```python
def base_b(x, b):
    rightmost_available_digit = ""
    while (x > 0):
        rightmost_available_digit += x % b
        x = x // b
    return int(rightmost_available_digit)
```
logb(n + 1) = digits in value

## Binary to Hex
Each group of 4 binary digits can be converted to one hex digit
