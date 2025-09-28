# More on Variables in Python

In this lecture, we dive deeper into variables in Python, exploring how they are stored in memory, how Python manages variable references, the concept of garbage collection, and how to work with constants and data types.

## Variables and Memory Address
- In Python, every variable points to a memory location where the actual data is stored.
- To check the memory address of a variable, we use the built-in `id()` function.

```python
num = 5
print(id(num))   # Example output: 2496052330864

name = 'navin'
print(id(name))  # Example output: 2496090712176
```

### Variable Assignment
When assigning the value of one variable to another, both variables may point to the same memory location if their values are the same.

```python
a = 10
b = a

print(a)         # 10
print(b)         # 10
print(id(a))     # Example: 2496052331024
print(id(b))     # Same as id(a)
```

- In Python, everything is an **object**.
- Variables act like **tags** that label these objects in memory.

```pyhton
print(id(10))    # Example: 2496052331024

k = 10
print(id(k))     # Same as above
```

### Reassignment and New Memory Address
If a variable is reassigned a new value, it points to a **new memory location.**

```python
a = 9
print(id(a))     # Example: 2496052330992

print(id(b))     # Still pointing to the old memory location
```

---


## Garbage Collection
- Python has an automatic garbage collector.
- If data in memory is **not referenced by any variable**, it becomes inaccessible and is removed automatically.

---


## Constants in Python
- Variables in Python can change values, but constants are intended to remain the same.
- By convention, constants are written in uppercase letters.

```python
PI = 3.14
print(PI)        # 3.14

# Though not enforced, changing it is possible:
PI = 3.15
print(PI)        # 3.15
```

> Python does not enforce immutability of constants. The uppercase naming is just a convention.

---


## Data Types
Python provides a wide variety of in-built data types such as:
- Integers (`int`)
- Floating-point numbers (`float`)
- Strings (`str`)
- Lists (`list`)
- Tuples (`tuple`)
- Dictionaries (`dict`)
- Sets (`set`)

To check the data type of a variable, use the `type()` function:
```python
PI = 3.15
print(type(PI))   # <class 'float'>
```

- Besides built-in types, Python also allows the creation of **custom data types** using **classes.**

----


## Summary
- Variables in Python are references to objects stored in memory.
- Multiple variables with the same value may point to the same memory location.
- Memory not referenced by variables is cleared by the garbage collector.
- Constants are represented by uppercase letters (convention, not enforced).
- Python supports multiple built-in data types and allows creation of custom types.

  
