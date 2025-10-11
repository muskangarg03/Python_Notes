# Break, Continue, and Pass in Python

In this lecture, we will learn about **loop control statements** — `break`, `continue`, and `pass`, which are used to alter the normal flow of execution within loops or conditional statements.


## Introduction

In Python, loops (`for` and `while`) generally execute a block of code repeatedly until a certain condition is false.  
However, sometimes we need more control over the flow of execution, for example:
- To exit a loop early
- To skip an iteration
- Or to write placeholder code that will be implemented later.

Python provides three special statements for these situations:
1. `break`
2. `continue`
3. `pass`



## The `break` Statement

The `break` statement is used to **terminate a loop prematurely** when a certain condition is met.  
Once the `break` statement is executed, the loop stops immediately and the program continues with the next statement after the loop.

**Syntax:**
```python
for variable in sequence:
    if condition:
        break
    # code block
```

### Example 1: Basic `break` Example
```python
for i in range(1, 6):
    if i == 3:
        break
    print(i)
```
**Output:**
```
1
2
```

### Example 2: `break` in a While Loop
```python
av = 5  # available candies
x = int(input("How many candies do you want? "))

i = 1
while i <= x:
    if i > av:
        print("Out of stock")
        break
    print("Candy")
    i += 1

print("Bye")
```


---


## The `continue` Statement

The `continue` statement is used to **skip the current iteration** of a loop and move to the **next iteration**,  
without executing the remaining code in the current loop cycle.

**Syntax:**
```python
for variable in sequence:
    if condition:
        continue
    # code block
```


### Example 1: Skipping a Value
```python
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
```
**Output:**
```
1
2
4
5
```

### Example 2: Skipping Multiples of 3 or 5
```python
for i in range(1, 101):
    if i % 3 == 0 or i % 5 == 0:
        continue
    print(i)

print("Bye")
```

### Example 3: Skipping Numbers Divisible by Both 3 and 5
```python
for i in range(1, 101):
    if i % 3 == 0 and i % 5 == 0:
        continue
    print(i)

print("Bye")
```


---


## The `pass` Statement

The `pass` statement acts as a **null operation**, it **does nothing** when executed.  
It serves as a placeholder when syntactically a statement is required, but you don’t want any command or code to execute.

It’s often used when:
- Writing code stubs (for future implementation)
- Maintaining the structure of a loop or function without executing anything inside.

**Syntax:**
```python
for variable in sequence:
    if condition:
        pass
    else:
        # code block
```


### Example 1: Using `pass` to Skip an Iteration
```python
for i in range(1, 6):
    if i == 3:
        pass
    else:
        print(i)
```
**Output:**
```
1
2
4
5
```

### Example 2: Using `pass` in Even Number Loop
```python
for i in range(1, 101):
    if i % 2 != 0:
        pass
    else:
        print(i)

print("Bye")
```
**Output:**
```
2
4
6
8
...
100
Bye
```


---


## Summary

| **Statement** | **Purpose** | **Effect on Loop Execution** | **Common Use Case** |
|----------------|-------------|-------------------------------|----------------------|
| `break` | Terminates the loop immediately | Exits the loop completely | Stop loop on a certain condition |
| `continue` | Skips the current iteration | Proceeds to next iteration | Skip specific values |
| `pass` | Does nothing (placeholder) | No effect, continues normally | Placeholder for future code |

