## Binary and Hexadecimal

### Slide 1: Number Systems

  * Computers store and process information using binary digits (bits).
  * Understanding different number systems helps in understanding how computers work at a low level.
  * **Decimal (Base-10):** The number system we use daily (digits 0-9).
  * **Binary (Base-2):** Uses only two digits: 0 and 1.
  * **Hexadecimal (Base-16):** Uses digits 0-9 and letters A-F.

### Slide 2: Binary (Base-2)

  * The fundamental language of computers.
  * Each digit is a "bit".
  * Numbers are represented as powers of 2.
  * Example: The binary number `1011` is:
      * (1 \* 2^3) + (0 \* 2^2) + (1 \* 2^1) + (1 \* 2^0) = 8 + 0 + 2 + 1 = 11 in decimal.

### Slide 3: Hexadecimal (Base-16)

  * A more compact way to represent binary numbers.
  * Each hexadecimal digit corresponds to 4 binary digits.
  * Digits: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A (10), B (11), C (12), D (13), E (14), F (15).
  * Example: The hexadecimal number `2B` is:
      * (2 \* 16^1) + (11 \* 16^0) = 32 + 11 = 43 in decimal.

### Slide 4: Example: Binary and Hex in Python

Python has built-in functions to convert numbers to their binary and hexadecimal representations.
```py

decimal_num = 42

# Convert to binary
binary_num = bin(decimal_num)
print(f"The decimal number {decimal_num} is {binary_num} in binary.")

# Convert to hexadecimal
hex_num = hex(decimal_num)
print(f"The decimal number {decimal_num} is {hex_num} in hexadecimal.")

# You can also write numbers in binary and hex directly
print(0b101010)  # Output: 42
print(0x2a)      # Output: 42

```
### Slide 5: Further Reading and Practice

  * **Further Reading:** While not a core focus of *Think Python*, you can find many online resources by searching for "binary and hexadecimal for programmers".
  * **Practice Exercise:**
      * Try to convert your age from decimal to binary and hexadecimal by hand.
      * Use Python's `bin()` and `hex()` functions to check your answers.