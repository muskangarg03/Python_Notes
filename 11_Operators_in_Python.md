# Operators in Python
Operators in Python are special symbols or keywords used to perform operations on values and variables. They are the foundation of expressions and logic building in Python programs.


## Types of Operators in Python
Python provides the following categories of operators:
1. Arithmetic Operators
2. Assignment Operators
3. Relational Operators
4. Logical Operators
5. Unary Operators

### 1. Arithmetic Operators
Used for performing **mathematical operations** such as addition, subtraction, multiplication, and division.

```python
x = 2
y = 3

print(x + y)  # 5 (Addition)
print(x - y)  # -1 (Subtraction)
print(x * y)  # 6 (Multiplication)
print(x / y)  # 0.666... (Division)
```

### 2. Assignment Operators
Used to assign values to variables.
- Basic assignment → =
- Shorthand assignment (operation + assignment together).

```python
x = 2
x = x + 2   # Normal assignment
print(x)    # 4

# Shorthand form
x += 2
print(x)    # 6

x *= 3
print(x)    # 18

# Multiple assignments in one line
a, b = 5, 6
print(a)    # 5
print(b)    # 6
```

### 3. Unary Operators
Unary operators work with a **single operand.**

```python
n = 7
print(n)   # 7

print(-n)  # -7 (Negation)

n = -n     # Re-assign with negated value
print(n)   # -7
```

### 4. Relational (Comparison) Operators
Used to compare values. These operators always return a Boolean result (True or False).

```python
a, b = 5, 6

print(a < b)   # True
print(a > b)   # False
print(a == b)  # False

a = 6
print(a == b)  # True
print(a < b)   # False
print(a <= b)  # True
print(a >= b)  # True
print(a != b)  # False

b = 7
print(a != b)  # True
```

### 5. Logical Operators
Logical operators are used to combine multiple conditions.
- **and** → Returns True only if both conditions are true.
- **or** → Returns True if at least one condition is true.
- **not** → Reverses the Boolean result.

```python
a = 5
b = 4

print(a < 8 and b < 5)   # True  (both true)
print(a < 8 and b < 2)   # False (one false)

print(a < 8 or b < 2)    # True  (one true)

x = True
print(x)         # True
print(not x)     # False

x = not x
print(x)         # False
```


---


## Truth Tables for Logical Operators

### 1. AND Operator (`and`)

The `and` operator returns **True** if *both conditions* are True. Otherwise, it returns **False**.

| A (Condition 1) | B (Condition 2) | A and B |
|-----------------|-----------------|---------|
| True            | True            | True    |
| True            | False           | False   |
| False           | True            | False   |
| False           | False           | False   |


### 2. OR Operator (`or`)

The `or` operator returns **True** if *any one condition* is True. It returns **False** only when both conditions are False.

| A (Condition 1) | B (Condition 2) | A or B  |
|-----------------|-----------------|---------|
| True            | True            | True    |
| True            | False           | True    |
| False           | True            | True    |
| False           | False           | False   |


### 3. NOT Operator (`not`)

The `not` operator reverses the value:  
- If the condition is True → returns False  
- If the condition is False → returns True  

| A (Condition) | not A |
|---------------|-------|
| True          | False |
| False         | True  |


### Example in Python

```python
a = True
b = False

print(a and b)   # False
print(a or b)    # True
print(not a)     # False
```


---


## Summary
- **Arithmetic operators** → Perform math operations.
- **Assignment operators** → Assign and update values.
- **Unary operators** → Work with a single operand.
- **Relational operators** → Compare values, return True/False.
- **Logical operators** → Combine multiple conditions with and, or, not.

These operators are essential in building Python expressions, conditions, and logic flow in programs.
