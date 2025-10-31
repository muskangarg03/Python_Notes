
# 28. Why NumPy? Installing NumPy in PyCharm


## Introduction

In Python, the built-in `array` module provides support for single-dimensional arrays — collections of elements of the same type.  
However, when it comes to handling multi-dimensional data (like matrices or tensors), or performing numerical computations efficiently, the built-in arrays are limited.  

This is where **NumPy (Numerical Python)** comes into play.  

NumPy is a powerful **library** that provides high-performance operations on large, **multi-dimensional arrays and matrices**, along with a vast collection of **mathematical functions.**


---


## Why NumPy?

The primary reason for using NumPy is its **support for multi-dimensional arrays** and **optimized numerical computation**.

### ➤ Limitation of Python’s `array` module
The standard Python `array` module supports only one-dimensional arrays.  
For example:

```python
from array import array

# Trying to create a multi-dimensional array
arr = array('i', [1, 2, 3], [4, 5, 6])
print(arr)
````

❌ Output:

```
TypeError: array() takes at most 2 arguments (3 given)
```

This means Python’s built-in `array` cannot handle multiple dimensions.



### ➤ NumPy Arrays

NumPy arrays can represent **n-dimensional data structures**, which makes them ideal for mathematical, statistical, and machine learning operations.

Example:

```python
from numpy import array

# Creating a 1D array
arr1 = array([1, 2, 3, 4, 5, 6])
print("1D Array:", arr1)

# Creating a 2D array
arr2 = array([[1, 2, 3], [4, 5, 6]])
print("2D Array:\n", arr2)
```

✅ Output:

```
1D Array: [1 2 3 4 5 6]
2D Array:
 [[1 2 3]
 [4 5 6]]
```


---


## Normal Array vs NumPy Array

| Feature                 | Python `array` Module        | NumPy Array (`ndarray`)        |
| ----------------------- | ---------------------------- | ------------------------------ |
| Dimensions              | Single (1D only)             | Multi-dimensional (nD)         |
| Type Specification      | Required (e.g. `'i'`, `'f'`) | Optional                       |
| Performance             | Slower                       | Much faster (C optimized)      |
| Mathematical Operations | Manual implementation        | Built-in vectorized operations |
| Memory Efficiency       | Moderate                     | Highly optimized               |


```
Python Array (1D):   [1, 2, 3, 4]

NumPy Array (2D):    [[1, 2, 3],
                      [4, 5, 6]]

NumPy Array (3D):    [[[1, 2], [3, 4]],
                      [[5, 6], [7, 8]]]
```

NumPy arrays generalize the idea of lists into higher dimensions efficiently.



### Example: Optional Type Specification in NumPy

Unlike the `array` module, NumPy doesn’t require explicit type specification, it detects data type automatically.

```python
from numpy import *

arr1 = array([1, 2, 3, 4, 5, 6])
print("Without Type Specification:", arr1)

arr2 = array([1, 2, 3, 4, 5, 6], int)
print("With Type Specification:", arr2)
```


---


## Installing NumPy

NumPy is not included with Python by default, you must install it manually.

### 1. Installing via Command Prompt (CMD)

Open your terminal or command prompt and run:

```bash
pip install numpy
```

If you are using Python 3, use:

```bash
pip3 install numpy
```

Once installed, you can verify the installation:

```bash
python
>>> import numpy
>>> numpy.__version__
```


### 2. Installing NumPy in PyCharm

1. Open **PyCharm**.
2. Press **`Ctrl + Alt + S`** (Windows/Linux) or **`Cmd + ,`** (macOS) to open **Settings**.
3. Navigate to **Project → Python Interpreter**.
4. Click on the **`+`** icon.
5. Search for **NumPy** and click **Install Package**.

Once installed, you can start importing it in your code:

```python
from numpy import *
arr = array([10, 20, 30, 40, 50])
print(arr)
```

Output:

```
[10 20 30 40 50]
```


---


## Advantages and Limitations

### Key Advantages of NumPy

| Advantage                     | Description                                                           |
| ----------------------------- | --------------------------------------------------------------------- |
| **Speed**                     | NumPy operations are much faster as they are implemented in C.        |
| **Multi-Dimensional Support** | Easily handles matrices, tensors, and n-dimensional data.             |
| **Mathematical Functions**    | Provides hundreds of built-in mathematical and statistical functions. |
| **Vectorized Operations**     | Supports element-wise operations without explicit loops.              |
| **Memory Efficiency**         | Consumes less memory compared to Python lists or arrays.              |


### Limitations of NumPy

| Limitation                       | Description                                                       |
| -------------------------------- | ----------------------------------------------------------------- |
| **Requires Installation**        | Not built-in; must be installed separately.                       |
| **Homogeneous Data**             | All elements in a NumPy array must be of the same type.           |
| **Complex Syntax for Beginners** | Requires understanding of vectorized operations and broadcasting. |


---


## Summary

* Python’s built-in `array` module supports only single-dimensional arrays.
* NumPy provides **multi-dimensional arrays (ndarrays)** and **high-performance numerical operations**.
* Installation can be done using **`pip install numpy`** (CMD) or via **PyCharm settings**.
* NumPy simplifies working with numerical data, making it a foundation for scientific computing in Python.

