# 26. Arrays in Python**


## Introduction to Arrays

An **array** is a data structure that stores **multiple items of the same data type** in a single variable.
It is **similar to a list**, but with one important difference:

>  **All elements in an array must be of the same type.**

Unlike lists, arrays are designed for **numeric computation**, and thus they are **more memory-efficient** when dealing with large datasets of numbers.


### Key Points

* Arrays can **grow or shrink dynamically** (no fixed size).
* Arrays are available through the **`array` module** in Python.
* You must **import** the module before creating arrays.


### Importing the Array Module

```python
import array

# OR (alias)
import array as arr

# OR (import all functions)
from array import *
```


### Syntax of Array Creation

```
vals = array('i', [5, 9, 8, 4, 2])
          ↓
+------+------+------+------+------+
|  5   |  9   |  8   |  4   |  2   |
+------+------+------+------+------+
   0      1      2      3      4   (Index) 
```

```python
from array import *

# array(typecode, [initial_values])
vals = array('i', [5, 9, 8, 4, 2])
print(vals)
```

Here:

* `'i'` → Type code representing signed integer
* `[5, 9, 8, 4, 2]` → Initial values of the array

Each block represents an element stored **sequentially in memory**.


---


## Type Codes in Arrays

Python arrays use **Type Codes** to specify the kind of data stored inside.
Each type code represents a specific C-style data type.

| Type Code | C Type        | Python Type | Size (bytes) | Description            |
| --------- | ------------- | ----------- | ------------ | ---------------------- |
| `'b'`     | signed char   | int         | 1            | Signed integer         |
| `'B'`     | unsigned char | int         | 1            | Unsigned integer       |
| `'i'`     | signed int    | int         | 2 or 4       | Default integer        |
| `'I'`     | unsigned int  | int         | 2 or 4       | Non-negative integer   |
| `'f'`     | float         | float       | 4            | Floating point         |
| `'d'`     | double        | float       | 8            | Double precision float |
| `'u'`     | Py_UNICODE    | char        | 2            | Unicode character      |


### Signed vs Unsigned Integers

* **Signed integers** can store both positive and negative numbers.
* **Unsigned integers** can store only non-negative values.

```python
from array import *

# Signed integers (allows negative values)
vals = array('i', [5, 9, -8, 4, 2])

# Unsigned integers (error if negative value used)
vals_unsigned = array('I', [5, 9, 8, 4, 2])
print(vals)
```


---


## Common Array Functions

### ➤ `buffer_info()`

Returns a tuple containing:

1. The **memory address** of the array
2. The **number of elements** stored in it

```python
vals = array('i', [5, 9, 8, 4, 2])
print(vals.buffer_info())
# Output → (address, length)
```


### ➤ `typecode`

Returns the type code of the array.

```python
print(vals.typecode)
# Output → i
```


### ➤ `append()`

Adds a new element to the end of the array.

```python
vals.append(10)
print(vals)
# Output → array('i', [5, 9, 8, 4, 2, 10])
```


### ➤ `remove()`

Removes the first occurrence of a specific element.

```python
vals.remove(8)
print(vals)
# Output → array('i', [5, 9, 4, 2])
```


### ➤ `reverse()`

Reverses the order of the array.

```python
vals.reverse()
print(vals)
# Output → array('i', [2, 4, 9, 5])
```


### Example: 

```python
from array import *

vals = array('i', [5, 9, 8, 4, 2])

print("Buffer Info:", vals.buffer_info())
print("Type Code:", vals.typecode)

vals.append(10)
vals.remove(8)
vals.reverse()

print("Final Array:", vals)
```


---


## Indexing and Accessing Elements

Array elements can be accessed using **index numbers**, starting from **0**.

```python
vals = array('i', [5, 9, 8, 4, 2])

print(vals[0])   # 5
print(vals[3])   # 4
```


### Get Array Length

```python
print(len(vals))   # Output → 5
```


### Array of Characters

```python
vals = array('u', ['a', 'e', 'i', 'o', 'u'])
print(vals)
# Output → array('u', 'aeiou')
```


---


## Traversing Arrays (Fetching Values)

There are **multiple ways** to fetch and display values from an array.

### 🔹 Using For Loop (with known length)

```python
for i in range(5):
    print(vals[i])
```


### 🔹 Using For Loop (unknown length)

```python
for i in range(len(vals)):
    print(vals[i])
```


### 🔹 Using Direct Iteration

```python
for e in vals:
    print(e)
```


### 🔹 Using While Loop

```python
i = 0
while i < len(vals):
    print(vals[i])
    i += 1
```


---


## Copying and Transforming Arrays

You can create a **new array** from an existing one, element by element.


### ➤ Copying Existing Array

```python
vals = array('i', [5, 9, 8, 4, 2])
newArr = array(vals.typecode, (a for a in vals))

for e in newArr:
    print(e)
```


### ➤ Creating a Derived Array (Square of Elements)

```python
vals = array('i', [5, 9, 8, 4, 2])
newArr = array(vals.typecode, (a*a for a in vals))

for e in newArr:
    print(e)
```

**Output:**

```
25
81
64
16
4
```


## Advantages of Using Arrays

* More **memory efficient** than lists (for numeric data).
* Faster for **numeric computation**.
* Supports **typecode-based data handling**.
* Can easily interface with **C code or low-level APIs**.


---


## Limitations of Arrays

* Can only store **one data type** at a time.
* Lacks some **flexible features of lists** (e.g., mixed data types).
* Requires **manual import** (`array` module).
* For advanced data operations, libraries like **NumPy** are preferred.

