# While Loop in Python


## Introduction to Loops

In programming, **loops** are used to execute a block of code **multiple times** until a certain condition is met.

Loops reduce redundancy by allowing repetition of statements without writing them multiple times.

Python provides two types of loops:
1. **`for` loop**
2. **`while` loop**


---


## Understanding the `while` Loop

A **`while` loop** executes a set of statements **as long as a condition is True**.  
Once the condition becomes False, the control **exits the loop** and continues with the next line of code after it.

### Key Features:
- Requires a **counter variable**
- Needs a **condition** to determine how long to execute
- Must include **increment** or **decrement** to prevent infinite loops


---


## Syntax of a `while` Loop

```python
# Initialization
counter_variable = starting_value

# While loop structure
while condition:
    statements
    incrementation_or_decrementation
```

### Essential Parts of a While Loop:
| Step | Description |
|------|--------------|
| **1. Initialization** | Set the starting value of the counter variable |
| **2. Condition** | The loop continues until this condition is False |
| **3. Update (Increment/Decrement)** | Modifies the counter variable each iteration |


---


## Examples of While Loops

### Example 1 — Basic Loop
```python
i = 1
while i <= 5:
    print("Telusko")
    i = i + 1
```

**Output:**
```
Telusko
Telusko
Telusko
Telusko
Telusko
```


### Example 2 — Decrementing Loop
```python
i = 5
while i >= 1:
    print("Telusko")
    i = i - 1
```

**Output:**
```
Telusko
Telusko
Telusko
Telusko
Telusko
```


### Example 3 — Printing Counter Values
```python
i = 5
while i >= 1:
    print("Telusko", i)
    i = i - 1
```

**Output:**
```
Telusko 5
Telusko 4
Telusko 3
Telusko 2
Telusko 1
```


---


## Nested While Loops

A **nested while loop** means one `while` loop inside another.  
It is useful when you need to repeat a block of code inside another repetition, like printing patterns or tables.

### Example 1 — Nested While with Decrementation
```python
i = 5
j = 1
while i >= 1:
    print("Telusko")
    while j <= 4:
        print("Rocks")
        j = j + 1
    i = i - 1
```

**Output:**
```
Telusko
Rocks
Rocks
Rocks
Rocks
```

> The **inner loop executes only once** because `j` is never reset to 1 for each iteration of `i`.


### Example 2 — Nested While with Proper Initialization
To make the nested loop work correctly for each iteration of the outer loop, we reset `j` inside the outer loop:

```python
i = 1
while i <= 5:
    j = 1
    print("Telusko")
    while j <= 4:
        print("Rocks")
        j = j + 1
    i = i + 1
    print()  # Print a blank line after each outer loop iteration
```

**Output:**
```
Telusko
Rocks
Rocks
Rocks
Rocks

Telusko
Rocks
Rocks
Rocks
Rocks

Telusko
Rocks
Rocks
Rocks
Rocks
```

> Each `Telusko` is now followed by 4 `Rocks` lines.


---


## The `end` Parameter in Python

By default, the `print()` function in Python **adds a newline** after each output.  
However, you can modify this behavior using the **`end` parameter**.

### Syntax:
```python
print(value, end=' ')
```

### Example:
```python
i = 1
while i <= 5:
    print(i, end=' ')
    i = i + 1
```

**Output:**
```
1 2 3 4 5
```

Here, instead of printing each number on a new line, all numbers are printed **on the same line**, separated by spaces.

### Note:
- `end=' '` → prints output in the same line with a space.
- `end=''` → prints outputs continuously without any space.
- `end='\n'` → default behavior (prints each output on a new line).


---


## Summary

| Concept | Description |
|----------|--------------|
| **While Loop** | Repeats a block of code while a condition is True |
| **Initialization** | Sets the starting value before entering the loop |
| **Condition** | Defines when to stop the loop |
| **Increment / Decrement** | Changes the loop variable to eventually stop the loop |
| **Nested While Loop** | A loop inside another loop |
| **end Parameter** | Controls how the output is separated (newline, space, etc.) |

