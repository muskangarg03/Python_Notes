# Number System Conversion in Python

This lecture covers the **Number System** in programming and the methods
to convert between different bases in Python.


## Introduction to Number Systems

A **number system** is a way of representing numbers using different
bases.

The most commonly used number systems in programming are:

1.  **Decimal (Base 10)** -- Uses digits 0--9.
2.  **Binary (Base 2)** -- Uses digits 0, 1. Widely used in computer
    systems.
3.  **Octal (Base 8)** -- Uses digits 0--7. Compact way to represent
    binary numbers.
4.  **Hexadecimal (Base 16)** -- Uses digits 0--9 and A--F. Often used
    in memory addresses and web colors.


---


## Decimal System (Base 10)

-   Everyday number system.
-   Example: 51 (decimal)

### Conversion Example (Decimal → Binary)

Divide by 2, record remainders, and read them in reverse:

2 \| 51 \| 1 2 \| 25 \| 1 2 \| 12 \| 0 2 \| 6 \| 0 2 \| 3 \| 1 2 \| 1 \|
1 0 Reverse → 110011

51 (decimal) → 110011 (binary)

``` python
bin(25)
# Output: '0b11001'
```


---


## Binary System (Base 2)

-   Only 0 and 1.
-   Computers use binary signals.

### Conversion Example (Binary → Decimal)

Binary: 11011

2\^4 2\^3 2\^2 2\^1 2\^0 1*16 + 1*8 + 0*4 + 1*2 + 1\*1 = 27

11011 (binary) → 27 (decimal)

``` python
int('0b11011', 2)
# Output: 27
```


---


## Octal System (Base 8)

-   Uses digits 0--7.
-   Compact way to represent binary.

### Conversion Example (Decimal → Octal)

Decimal: 51

8 \| 51 \| 3 8 \| 6 \| 6 8 \| 0 \| 0 Reverse → 63

51 (decimal) → 63 (octal)

``` python
oct(25)
# Output: '0o31'

int('0o31', 8)
# Output: 25
```


---


## Hexadecimal System (Base 16)

-   Uses digits 0--9 and A--F.
-   Very common in programming.

### Conversion Example (Decimal → Hexadecimal)

Decimal: 51

16 \| 51 \| 3 16 \| 3 \| 3 16 \| 0 \| 0 Reverse → 33

51 (decimal) → 33 (hexadecimal)

``` python
hex(25)
# Output: '0x19'

hex(10)
# Output: '0xa'

int('0x33', 16)
# Output: 51
```


---


## Other Conversions

### Octal ↔ Binary

**Octal to Binary**: Replace each octal digit with 3-bit binary. -
Example: 725 (octal) → 111010101 (binary)

**Binary to Octal**: Group binary digits into 3-bit sets. - Example:
101011011 (binary) → 533 (octal)


---


## Python Built-in Functions for Conversion  

| Conversion              | Function   | Example              | Output      |
|--------------------------|------------|----------------------|-------------|
| Decimal → Binary         | `bin(x)`   | `bin(51)`            | `'0b110011'` |
| Binary → Decimal         | `int(x,2)` | `int('0b110011', 2)` | `51`        |
| Decimal → Octal          | `oct(x)`   | `oct(51)`            | `'0o63'`    |
| Octal → Decimal          | `int(x,8)` | `int('0o63', 8)`     | `51`        |
| Decimal → Hexadecimal    | `hex(x)`   | `hex(51)`            | `'0x33'`    |
| Hexadecimal → Decimal    | `int(x,16)`| `int('0x33', 16)`    | `51`        |


---


## Summary

-   **Decimal**: Base 10, digits 0--9.
-   **Binary**: Base 2, digits 0--1.
-   **Octal**: Base 8, digits 0--7.
-   **Hexadecimal**: Base 16, digits 0--9, A--F.
-   Python provides **direct built-in methods** (bin(), oct(), hex(),
    int()) for conversion between these systems.

