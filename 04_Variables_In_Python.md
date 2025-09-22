# Variables in Python

A variable is a named container used to store data (value).  
In Python, variables are created automatically when a value is assigned to them.  

### Example:
```python
x = 2          # x is the variable, 2 is the value
print(x + 3)   # Output: 5

y = 3
print(x + y)   # Output: 5
```

- Variables are **mutable**, meaning their values can be changed during execution.  
```python
x = 9
print(x)      # Output: 9
print(x + y)  # Output: 12
```

---

## Accessing Undefined Variables
If you try to use a variable that is not defined, Python throws a **NameError**.  

### Example:
```python
abc
# Traceback (most recent call last):
# NameError: name 'abc' is not defined. Did you mean: 'abs'?
```

---

## Using the Underscore `_`  
Python automatically stores the result of the last executed expression in the variable `_`.  

### Example:
```python
x = 5
y = 3
x + y        # Output: 8
_ + y        # Output: 11 (since _ stores previous output 8)
```

---

## Strings as Variables
- Strings in Python can be written using **single (‘ ’)** or **double (“ ”)** quotes.  
- Variables can store string values just like numbers.  

### Example:
```python
name = "youtube"
print(name)             # Output: youtube
print(name + " rocks")  # Output: youtube rocks
```

Incorrect concatenation:
```python
print(name ' rocks')  # SyntaxError
```

---

## String Indexing and Slicing  

### (a) Positive Indexing
Each character in a string has an index:  
```
y   o   u   t   u   b   e
0   1   2   3   4   5   6
```

### (b) Negative Indexing
Python also supports negative indexing:  
```
y   o   u   t   u   b   e
-7 -6  -5  -4  -3  -2  -1
```

### Examples:
```python
name = "youtube"

print(name[0])     # 'y'
print(name[6])     # 'e'
print(name[-1])    # 'e'

print(name[0:2])   # 'yo'  (characters from index 0 to 1)
print(name[1:4])   # 'out'
print(name[1:])    # 'outube' (from index 1 till end)
print(name[:4])    # 'yout'
print(name[3:10])  # 'tube' (index out of range is ignored)
print(name[-5:-2]) # 'utu'
```

### Special Cases:
```python
print(name[:])     # 'youtube'  (entire string)
print(name[:0])    # '' (empty string)
```

---

## Strings are Immutable  
In Python, **strings cannot be modified** once created.  
Attempting to assign new characters to existing string indices results in an error.  

### Example:
```python
name = "youtube"
name[0] = "r"  
# TypeError: 'str' object does not support item assignment
```

---

## String Concatenation
Strings can be joined using the `+` operator.  

### Example:
```python
name = "youtube"
print("my " + name[3:])   # Output: my tube
```

---

## Built-in Function: `len()`  
The `len()` function returns the total number of characters in a string.  

### Example:
```python
myname = "Navin Reddy"
print(len(myname))   # Output: 11
```

---

## Summary
- Variables are containers for values and can be reassigned.  
- Using an undefined variable raises a NameError.  
- `_` stores the last evaluated result.  
- Strings can be assigned, concatenated, sliced, and indexed.  
- Strings are **immutable** (cannot be changed after creation).  
- `len()` is used to find the length of a string.  
