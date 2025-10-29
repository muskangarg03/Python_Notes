# 23. Printing Patterns in Python

In this lecture, we will learn how to implement the logic behind **pattern printing in Python**.


## Introduction to Pattern Printing

Pattern printing improves your **logical thinking** and **problem-solving** abilities.
Programming is all about solving problems — you must understand the requirement and then write code to implement it.

A pattern can be printed in multiple ways in Python.
Let’s start with the simplest approach: **printing multiple `#` characters**.


### Example 1: Printing a Row of Hashes

```python
print("# # # #")
```

### **Output:**

```
# # # #
```

In this example, all hashes are printed in a single line because they are part of a single string.



### Example 2: Printing Hashes Vertically (One per Line)

```python
print("# ")
print("# ")
print("# ")
print("# ")
```

### **Output:**

```
#
#
#
#
```

Here, each `print()` statement starts a **new line**, resulting in a **column of hashes**.



### Example 3: Printing Hashes in a Row Using `end=""`

If you are allowed to print only one `#` per statement but want them in a row, you can use the `end` parameter.

```python
print("# ", end="")
print("# ", end="")
print("# ", end="")
print("# ", end="")
```

### **Output:**

```
# # # #
```

**Explanation:**

* The `end` parameter in `print()` prevents the cursor from moving to the next line.
* Instead of the default newline (`\n`), it uses a space `" "` to separate each print.


---


## Using Loops for Efficient Pattern Printing

Writing the same `print()` statement multiple times is repetitive.
We can use **loops** to make the code more efficient and dynamic.


### Example 4: Using a `for` Loop to Print a Row

```python
for j in range(4):
    print("# ", end="")
```

### **Output:**

```
# # # #
```

**Explanation:**

* The loop runs **4 times (0 to 3)**.
* Each iteration prints one `#` symbol followed by a space.
* The `end=""` prevents a newline after each print.



### Example 5: Printing Multiple Rows (Square Pattern)

We can print multiple rows by adding another loop — an **outer loop** for rows and an **inner loop** for columns.

```python
for i in range(4):              # Outer loop → rows
    for j in range(4):          # Inner loop → columns
        print("# ", end="")
    print()                     # Moves to the next line after each row
```

### **Output:**

```
# # # #
# # # #
# # # #
# # # #
```

**Explanation:**

* The **outer loop** runs 4 times (for 4 rows).
* The **inner loop** prints 4 hashes in each row.
* After each row, `print()` moves the cursor to the next line.
This creates a **4×4 square** pattern.


---


## Printing a Right-Triangle Pattern

We can modify the loop condition to form a **right-angled triangle** pattern.
Instead of printing the same number of symbols in each row, we’ll print **incrementally more** in each subsequent row.


### Example 6: Right-Triangle Pattern

```python
for i in range(4):
    for j in range(i + 1):
        print("# ", end="")
    print()
```

### **Output:**

```
# 
# # 
# # # 
# # # # 
```

**Explanation:**

* The outer loop controls the number of rows.
* The inner loop prints `i + 1` hashes in each row.
* As `i` increases, the number of hashes increases, forming a right triangle.



## Printing a Reverse Right-Triangle Pattern

To print a **reverse right triangle**, we simply reduce the number of hashes in each row.


### Example 7: Reverse Right-Triangle Pattern

```python
for i in range(4):
    for j in range(4 - i):
        print("# ", end="")
    print()
```

### **Output:**

```
# # # #
# # #
# #
#
```

**Explanation:**

* The outer loop still represents rows.
* The inner loop runs for `(4 - i)` times, printing fewer hashes with each iteration.
* This produces a **reverse triangle**.


---


## Summary 

| Pattern Type               | Outer Loop Controls | Inner Loop Controls                    | Example Output          |
| -------------------------- | ------------------- | -------------------------------------- | ----------------------- |
| **Square**                 | Number of rows      | Number of columns (constant)           | 4×4 square              |
| **Right Triangle**         | Number of rows      | Columns increase with each row (`i+1`) | Triangle from top-left  |
| **Reverse Right Triangle** | Number of rows      | Columns decrease with each row (`n-i`) | Triangle from top-right |

