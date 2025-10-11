# 22.1 Break vs Continue vs Pass in Python  


In Python, loop control statements — `break`, `continue`, and `pass` are used to modify the normal flow of execution inside loops or functions. They help control how iterations behave and provide flexibility in managing conditions inside loops.



## 1. `continue` Statement

The `continue` statement **skips the current iteration** of the loop and moves to the **next iteration**, without executing the remaining statements inside the loop for that iteration.

### **Syntax:**
```python
for i in range(5):
    if i == 3:
        continue
    print("Hello", i)
```

### **Output:**
```
Hello 0
Hello 1
Hello 2
Hello 4
```

### **Explanation:**
- When `i == 3`, the `continue` statement is executed.  
- The loop **skips the `print()` statement** for `i = 3` and jumps to the next iteration.  
- The loop then continues normally for `i = 4`.

**Use Case:**  
When you want to skip specific iterations without terminating the entire loop.


---


## 2. `break` Statement

The `break` statement **terminates the entire loop** immediately, regardless of the loop condition or remaining iterations.

### **Syntax:**
```python
for i in range(5):
    if i == 3:
        break
    print("Hello", i)
```

### **Output:**
```
Hello 0
Hello 1
Hello 2
```

### **Explanation:**
- When `i == 3`, the `break` statement is executed.  
- The loop **stops immediately**, and no further iterations are performed.  
- Unlike `continue`, which only skips one iteration, `break` **ends the entire loop**.

**Use Case:**  
When a certain condition is met and you want to exit the loop early.


---


## 3. `pass` Statement

The `pass` statement acts as a **null operation**, it does nothing when executed.  
It’s used as a **placeholder** for future code, allowing you to define empty functions, classes, or loops without causing syntax errors.

### **Syntax:**
```python
def func():
    pass
```

### **Explanation:**
- Normally, a function body cannot be empty in Python, it will raise an `IndentationError`.
- The `pass` statement allows defining a **syntactically valid structure** even when the logic is not yet implemented.

**Use Case:**  
When you’re outlining code (like a class, function, or loop) and want to avoid syntax errors before implementing actual logic.


---


## Summary

| Statement | Function | Effect on Loop | Common Use Case |
|------------|-----------|----------------|------------------|
| **continue** | Skips current iteration | Goes to next iteration | Skip specific conditions |
| **break** | Exits loop entirely | Stops loop execution | Stop on condition met |
| **pass** | Does nothing | No effect | Placeholder for future code |


### Example: Using All Three Together
```python
for i in range(6):
    if i == 2:
        continue     # Skip iteration for i = 2
    elif i == 4:
        break        # Stop loop at i = 4
    else:
        print("Processing:", i)
else:
    pass              # Placeholder (won’t execute unless no break)
```

### **Output:**
```
Processing: 0
Processing: 1
Processing: 3
```


---


### Key Takeaways
- **`continue`** → Skip this iteration.  
- **`break`** → Stop the loop entirely.  
- **`pass`** → Do nothing; used as a placeholder.  

Together, these control statements help manage loop flow, conditional logic, and code structuring efficiently.
