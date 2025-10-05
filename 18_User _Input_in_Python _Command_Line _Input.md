# User Input in Python | Command Line Input


## 1. Getting User Input  

Python provides an easy way to get user input using the **`input()`** function.  
It pauses the program and waits for the user to type something and press Enter.  

### Example:
```python
name = input("Please enter your name: ")
x = input("Enter first number: ")
y = input("Enter second number: ")
z = x + y
print(z)
```

**Output:**
```
Enter first number: 9  
Enter second number: 5  
95
```

> Note: The output is `95` because the `input()` function returns a **string** by default.  


---


## 2. The `input()` Function  

The **`input()`** function accepts user input from the command line.  

```python
name = input("Enter your name: ")
print(name)
```

The `input()` function always returns a **string**.  
If you want to use the input as a number, convert it using `int()` or `float()`.


---


## 3. Type Conversion  

Since all input values are returned as **strings**, we must convert them to perform arithmetic.  

### Example:
```python
x = input("Enter first number: ")
y = input("Enter second number: ")
a = int(x)
b = int(y)
z = a + b
print(z)
```

**Output:**
```
Enter first number: 9  
Enter second number: 5  
14
```

Instead of creating extra variables, we can simplify this:

```python
x = int(input("Enter first number: "))
y = int(input("Enter second number: "))
z = x + y
print(z)
```


---


## 4. Using Index Value  

You can access a single character from user input using indexing.

### Example:
```python
ch = input("Enter a character: ")
print(ch[0])
```

or directly:

```python
ch = input("Enter a character: ")[0]
print(ch)
```


---


## 5. `eval()` Function  

The **`eval()`** function evaluates the input as a Python expression and returns the result.  

### Example:
```python
x = eval(input("Enter an expression: "))
print(type(x))
```

Example input/output:
```
Enter an expression: 9 + 5
<class 'int'>
```

Another example:
```python
result = eval(input("Enter an expression: "))
print(result)
```

**Output:**
```
Enter an expression: 2 + 3 * 5
17
```


---


## 6. Command-Line Arguments  

Python’s **`sys`** module allows passing values from the command line.  
Use **`sys.argv`** to access the command-line arguments.

### Example (`Mycode.py`)
```python
import sys

x = sys.argv[1]
y = sys.argv[2]
z = x + y
print(z)
```

**Command:**
```
python Mycode.py 9 5
```

**Output:**
```
95
```

Here:
- `Mycode.py` → Argument 0  
- `9` → Argument 1  
- `5` → Argument 2  

Since these are strings, the result is concatenation.  
To fix this, convert inputs to integers:

```python
import sys

x = int(sys.argv[1])
y = int(sys.argv[2])
z = x + y
print(z)
```

**Command:**
```
python Mycode.py 9 5
```

**Output:**
```
14
```


---


## Summary  

| Concept | Description | Example |
|----------|--------------|----------|
| `input()` | Takes user input as a string | `x = input("Enter name: ")` |
| Type Conversion | Converts string input to number | `int(input("Enter number: "))` |
| Indexing | Access specific character | `input("Enter: ")[0]` |
| `eval()` | Evaluates an expression | `eval(input("Enter expr: "))` |
| Command-line Input | Takes arguments via terminal | `sys.argv` |

