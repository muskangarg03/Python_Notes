# Conditional Statements in Python


## 1. CPU Units Overview

The **CPU (Central Processing Unit)** is the brain of the computer. It has **three main units**:

| Unit | Full Form | Function |
|------|------------|-----------|
| **CU** | Control Unit | Controls the flow of data and instructions |
| **ALU** | Arithmetic Logic Unit | Performs mathematical and logical operations |
| **MU** | Memory Unit | Stores variables and data |

The **ALU** itself has two parts:
- **AU (Arithmetic Unit):** Performs mathematical operations like addition, subtraction, etc.
- **LU (Logical Unit):** Performs logical operations and comparisons, helping the computer make decisions.


---


## 2. Conditional Statements in Python

### What are Conditional Statements?

In programming, **conditional statements** allow you to control the **flow of execution** based on certain conditions.  
Python uses keywords like `if`, `elif`, and `else` to apply conditions in code.


---


## 3. The `if` Statement

The `if` statement executes a block of code **only if** a specified condition is `True`.

### Syntax:
```python
if condition:
    statement(s)
```

### Example:
```python
if True:
    print("I'm right")
```

**Output:**
```
I'm right
```

If the condition is **False**, the block is **skipped**:
```python
if False:
    print("I'm right")
print("Bye")
```

**Output:**
```
Bye
```


---


## 4. Indentation in Python

**Indentation** refers to spaces at the beginning of a code line.  
It is **mandatory** in Python to define blocks of code.

- Defines code blocks (like if, for, while)
- Increases readability
- Avoids ambiguity

### Example1:
```python
x = 3
r = x % 2
if r == 0:
    print("Even")
print("Bye")
```

**Output:**
```
Bye
```

Since `r == 0` is False, the print inside the `if` block is skipped.


---


### Example2:
```python
x = 8
r = x % 2
if r == 0:
    print("Even")
if r == 1:
    print("Odd")
print("Bye")
```

**Output:**
```
Even
Bye
```


---


## 5. The `else` Block

The `else` block executes **only when** the condition in the `if` statement is **False**.

### Example:
```python
x = 8
r = x % 2
if r == 0:
    print("Even")
else:
    print("Odd")
print("Bye")
```

**Output:**
```
Even
Bye
```

The use of `else` improves **efficiency** — it prevents redundant checks that multiple standalone `if` statements would perform.


---


## 6. Nested `if` and `else` Statements

A nested `if` statement means **one `if` block inside another**.  
It allows you to check **multiple conditions** in a structured manner.

### Example:
```python
x = 8
r = x % 2
if r == 0:
    print("Even")
    if x > 5:
        print("Great")
    else:
        print("Not so great")
else:
    print("Odd")
print("Bye")
```

**Output:**
```
Even
Great
Bye
```

The **inner `if`** is checked **only if** the **outer `if`** condition is True.


---


## 7. The `if`, `elif`, and `else` Chain

When multiple conditions need to be checked in sequence, Python provides the **`elif`** (short for *else if*) keyword.

### Syntax:
```python
if condition1:
    statement1
elif condition2:
    statement2
elif condition3:
    statement3
else:
    statement4
```

### Example:
```python
x = 2
if x == 1:
    print("One")
elif x == 2:
    print("Two")
elif x == 3:
    print("Three")
elif x == 4:
    print("Four")
else:
    print("Wrong Input")
```

**Output:**
```
Two
```

### Key Notes:
- Only **one block** among `if`, `elif`, and `else` executes.
- Once a condition is **True**, the rest are **skipped**.
- The final `else` block is **optional**, used as a fallback.


---


## Comparison: Multiple `if` vs `if-elif-else`

### Multiple `if` Statements:
```python
x = 2
if x == 1:
    print("One")
if x == 2:
    print("Two")
if x == 3:
    print("Three")
if x == 4:
    print("Four")
```

> All conditions are **checked individually**.

---

### Using `if-elif-else`:
```python
x = 2
if x == 1:
    print("One")
elif x == 2:
    print("Two")
elif x == 3:
    print("Three")
elif x == 4:
    print("Four")
else:
    print("Wrong Input")
```

> Stops checking **after the first True condition** — more **efficient**.


---


## Summary

| Concept | Description |
|----------|--------------|
| `if` | Executes a block when condition is True |
| `else` | Executes when `if` condition is False |
| `elif` | Checks additional conditions |
| **Indentation** | Defines the structure and hierarchy of code |
| **Nested if** | An `if` inside another `if` for multi-level conditions |

