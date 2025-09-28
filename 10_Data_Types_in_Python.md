# 10. Data Types in Python

In Python, **data types** define the kind of values a variable can hold and how those values can be manipulated.  
Python is **dynamically typed**, meaning you don’t need to explicitly declare the data type of a variable — it is inferred at runtime based on the value assigned.  

## Built-in Data Types in Python

### 1. **NoneType**
Represents the **absence of a value**.

```python
a = None
print(type(a))   # <class 'NoneType'>
```

---

### 2. Numbers
Python supports three numeric types:
- Integers (`int`) → whole numbers
- Floating-point numbers (`float`) → decimal values
- Complex numbers (`complex`) → real + imaginary part

```python
# Integer
a = 5
print(type(a))   # <class 'int'>

# Float
num = 2.5
print(type(num)) # <class 'float'>

# Complex
c = 2 + 9j
print(type(c))   # <class 'complex'>
```

**Type Conversion**
```pyhton
a = 5.6
b = int(a)       # float → int
print(b, type(b))  # 5 <class 'int'>

k = float(b)     # int → float
print(k, type(k))  # 5.0 <class 'float'>

c = complex(4, 5)  # create complex number
print(c, type(c))  # (4+5j) <class 'complex'>
```

---

### 3. Boolena(`bool`)
Booleans represent logical values: **True or False.**
Internally stored as integers (`True = 1`, `False = 0`).

```python
a = True
print(type(a))   # <class 'bool'>

b = 3 < 5
print(b)         # True
print(type(b))   # <class 'bool'>

print(int(True))    # 1
print(int(False))   # 0
print(float(False)) # 0.0
```

---

### 4. Sequence Data Types
Sequences allow storing multiple values. Common ones are:
- List
- Tuple
- Set
- String
- Range

**(i) List**
- Ordered, mutable collection.
- Enclosed in [ ].
- Allows duplicates.

```python
lst = [25, 36, 45, 12]
print(lst)          # [25, 36, 45, 12]
print(type(lst))    # <class 'list'>
```

**(ii) Tuple**
- Ordered, immutable collection.
- Enclosed in ( ).
- Useful for storing data that should not change.

```python
t = (25, 36, 45, 25, 12)
print(t)            # (25, 36, 45, 25, 12)
print(type(t))      # <class 'tuple'>
```

**(iii) Set**
- Unordered, mutable, collection of unique elements.
- Enclosed in { }.
- Removes duplicates automatically.

```python
s = {25, 36, 45, 26, 24, 25}
print(s)            # {36, 24, 25, 26, 45}
print(type(s))      # <class 'set'>
```

**(iv) String**
- A sequence of characters, enclosed in ' ' or " ".
- Strings are immutable.

```python
str1 = "hello"
print(str1)         # hello
print(type(str1))   # <class 'str'>

ch = 'a'
print(ch, type(ch)) # 'a' <class 'str'>
```

**(v) Range**
- Represents a sequence of numbers.
- Immutable, commonly used in loops.

```python
r = range(10)
print(r)               # range(0, 10)
print(type(r))         # <class 'range'>

print(list(range(10)))      # [0,1,2,3,4,5,6,7,8,9]
print(list(range(2,10,2)))  # [2,4,6,8]
```

---

### 5. Dictionary (`dict`)
- Stores key-value pairs.
- Keys must be unique and immutable.
- Enclosed in { }.

```python
d1 = {'navin':'samsung', 'rahul':'iPhone', 'kiran':'oneplus'}
print(d1)            # {'navin':'samsung', 'rahul':'iPhone', 'kiran':'oneplus'}

print(d1.keys())     # dict_keys(['navin', 'rahul', 'kiran'])
print(d1.values())   # dict_values(['samsung', 'iPhone', 'oneplus'])

print(d1['rahul'])   # iPhone
print(d1.get('kiran')) # oneplus
```

---

## Summary
- NoneType → represents no value.
- Numbers → int, float, complex.
- Boolean → True / False.
- Sequences →
    - List (mutable, ordered)
    - Tuple (immutable, ordered)
    - Set (mutable, unordered, unique elements)
    - String (immutable sequence of characters)
    - Range (immutable sequence of numbers)
- Dictionary → key-value pairs.

- These data types form the foundation of Python programming.
- You can also define custom data types using classes.
