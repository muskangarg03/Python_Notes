# Import Math Functions in Python  

In this lecture, we will learn about the math module in Python, its functions, constants, and how to import them properly.  



## Introduction  

- The **`math` module** in Python provides a wide range of **mathematical functions and constants**.  
- It is a **built-in module**, so no external installation is required.  
- The `math` module is commonly used for:  
  - Square root  
  - Power calculations  
  - Floor & Ceil functions  
  - Trigonometric functions  
  - Logarithmic and exponential functions  

---

## Importing the Math Module  

You must import the module before using its functions:  

```python
import math

# Example
x = math.sqrt(25)
print(x)   # 5.0
```

### Different Ways to Import  

1. **Import entire module**  
   ```python
   import math
   print(math.sqrt(25))
   ```

2. **Using alias**  
   ```python
   import math as m
   print(m.sqrt(25))
   ```

3. **Import specific functions**  
   ```python
   from math import sqrt, pow
   print(sqrt(25))   # 5.0
   print(pow(2, 3))  # 8.0
   ```

If you directly call `sqrt(25)` without importing it, you’ll get a `NameError`.  


---


## Commonly Used Math Functions  

| Function | Description | Example | Output |
|----------|-------------|---------|--------|
| `math.sqrt(x)` | Square root of `x` | `math.sqrt(25)` | `5.0` |
| `math.pow(x, y)` | `x` raised to power `y` | `math.pow(3, 2)` | `9.0` |
| `math.ceil(x)` | Smallest integer ≥ `x` | `math.ceil(3.3)` | `4` |
| `math.floor(x)` | Largest integer ≤ `x` | `math.floor(3.3)` | `3` |
| `math.exp(x)` | Exponential `e^x` | `math.exp(2)` | `7.389...` |
| `math.log(x)` | Natural logarithm (base *e*) | `math.log(10)` | `2.302...` |
| `math.log(x, base)` | Logarithm with custom base | `math.log(8, 2)` | `3.0` |
| `math.sin(x)` | Sine of `x` (in radians) | `math.sin(math.pi/2)` | `1.0` |
| `math.cos(x)` | Cosine of `x` | `math.cos(0)` | `1.0` |
| `math.tan(x)` | Tangent of `x` | `math.tan(math.pi/4)` | `1.0` |


---


## Math Constants  

The `math` module provides useful constants:  

| Constant | Description | Example | Output |
|----------|-------------|---------|--------|
| `math.pi` | Value of π | `print(math.pi)` | `3.141592653589793` |
| `math.e` | Euler’s number | `print(math.e)` | `2.718281828459045` |
| `math.inf` | Infinity | `print(math.inf)` | `inf` |
| `math.nan` | Not a Number | `print(math.nan)` | `nan` |


---


## Exploring the Math Module  

To see all available functions and attributes:  

```python
import math
print(dir(math))
```

Output (partial list):  
```
['acos', 'asin', 'atan', 'ceil', 'comb', 'cos', 'degrees', 
 'dist', 'e', 'exp', 'factorial', 'floor', 'fmod', 'gcd', 
 'hypot', 'inf', 'isclose', 'isfinite', 'isinf', 'isnan',
 'log', 'log10', 'pow', 'prod', 'radians', 'sin', 'sqrt', 'tan', 'tau']
```

To get detailed documentation:  

```python
help(math)
```


---


## Summary  

- The **`math` module** allows us to perform advanced mathematical calculations.  
- We can import the entire module, use an alias, or import specific functions.  
- It provides both **functions** (sqrt, pow, log, sin, cos, etc.) and **constants** (pi, e, inf, nan).  
- Using `dir(math)` and `help(math)` helps explore available functions and documentation.  

