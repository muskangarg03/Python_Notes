
# Python Bitwise Operators  


## Bitwise Operators
- In **bitwise operations**, integers are first converted into **binary form**.  
- Operators perform actions on each **bit** (or corresponding pair of bits).  
- The final **result is returned in decimal format**.  

There are six bitwise operators in Python:  
1. Complement (~)
2. AND (&)
3. OR (|)
4. XOR (^) 
5. Left Shift (<<)
6. Right Shift (>>)


---


## Complement Operator (`~`)  
- Also known as **tilde (`~`) operator**.  
- It flips all bits of the number:  
  - `0 → 1`  
  - `1 → 0`  
- This produces the **1’s complement**.  
- Since computers store negative numbers in **2’s complement**, the final result is:  
  ```
  ~x = -(x + 1)
  ```

### Example: `~12`  
```python
>>> ~12
-13
```

### Explanation:  
```
Decimal:  12
Binary :  00001100
1's Comp: 11110011
2's Comp: 11110011 + 1 = 11110100 (Decimal -13)
```


---


## AND Operator (`&`)  
- Returns **1** only if both corresponding bits are **1**.  
- Otherwise returns **0**.  

### Example: `12 & 13`  
```python
>>> 12 & 13
12
```

### Conversion:  
```
12 → 1100
13 → 1101
--------------
AND → 1100 = 12
```

### Example: `25 & 30`  
```python
>>> 25 & 30
24
```

```
25 → 11001
30 → 11110
--------------
AND → 11000 = 24
```


---


## OR Operator (`|`)  
- Returns **1** if at least one corresponding bit is **1**.  
- Returns **0** only when both bits are **0**.  

### Example: `12 | 13`  
```python
>>> 12 | 13
13
```

```
12 → 1100
13 → 1101
--------------
OR  → 1101 = 13
```


---


## XOR Operator (`^`)  
- Returns **1** when there is an **odd number of 1s** in the bits.  
- Returns **0** when the number of `1`s is even.  

### Example: `12 ^ 13`  
```python
>>> 12 ^ 13
1
```

```
12 → 1100
13 → 1101
--------------
XOR → 0001 = 1
```

### Example: `25 ^ 30`  
```python
>>> 25 ^ 30
7
```

```
25 → 11001
30 → 11110
--------------
XOR → 00111 = 7
```


---



## Left Shift (`<<`)  
- Shifts bits **to the left** by a given number of positions.  
- Each shift left multiplies the number by `2`.  

### Example: `10 << 2`  
```python
>>> 10 << 2
40
```

```
10 → 00001010
Shift Left (2) → 00101000 = 40
```


---



## Right Shift (`>>`)  
- Shifts bits **to the right** by a given number of positions.  
- Each shift right divides the number by `2`.  

### Example: `10 >> 2`  
```python
>>> 10 >> 2
2
```

```
10 → 00001010
Shift Right (2) → 00000010 = 2
```


---


## Summary of Bitwise Operators  

| Operator | Symbol | Description |
|----------|--------|-------------|
| Complement | `~`  | Flips all bits (1’s complement, stored as 2’s complement) |
| AND       | `&`  | 1 if both bits are 1 |
| OR        | `|`  | 1 if at least one bit is 1 |
| XOR       | `^`  | 1 if odd number of 1s |
| Left Shift | `<<` | Shifts bits left (multiply by 2) |
| Right Shift | `>>` | Shifts bits right (divide by 2) |


---


Bitwise operators are commonly used in:  
- Low-level programming  
- Cryptography  
- Networking (IP masking, subnetting)  
- Hardware-level operations  
