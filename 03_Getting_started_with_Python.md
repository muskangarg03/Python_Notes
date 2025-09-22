# Getting Started With Python

Python is a high-level, interpreted language designed to be easy to read and write. The interpreter translates Python code into bytecode and executes it, ultimately running machine-level instructions.

We use programming languages like Python because computers only understand binary (0s and 1s), programming languages provide a human-friendly way to write instructions that get translated into machine code.

We're using Python IDLE in this lecture as **Python IDLE** is a simple environment where you can run code interactively or save scripts as .py files and execute them from an editor or terminal.

## Airthmetic Operations
Python supports the standard arithmetic operators. Below each operator is explained and illustrated with examples and expected output.

### Addition `+`

```python
>>> 2 + 3
5
```

*Adds two numbers.*

### Subtraction `-`

```python
>>> 9 - 8
1
```

*Subtracts the right-hand operand from the left-hand operand.*

### Multiplication `*`

```python
>>> 4 * 6
24
```

*Multiplies operands.*

### True division `/` (returns `float`)

* The division operator `/` always returns a float even if both operands are integers.

```python
>>> 8 / 4
2.0
>>> 5 / 2
2.5
```

*This is useful because division can produce non-integer results; returning a float preserves precision.*

### Floor (integer) division `//`

* Use `//` if you want only the integer part (the quotient) and to discard any fractional remainder.

```python
>>> 10 // 3
3
>>> -7 // 3
-3  # floor division rounds toward negative infinity
```

> Note: with negative numbers `//` performs floor division — results may look unintuitive if you expect truncation toward zero.*

### Modulus `%` (remainder)

```python
>>> 10 % 3
1
```

*Returns remainder of division.*

### Exponentiation `**`

```python
>>> 2 ** 3
8
>>> 4 ** 0.5
2.0  # square root
```

*Raises the left operand to the power of the right operand.*

### Operator precedence and parentheses

Python obeys the usual mathematical rules (BODMAS). Use parentheses to change order.

```python
>>> 8 + 2 * 3
14
>>> (8 + 2) * 3
30
```

**Common pitfall:** incomplete expressions cause syntax errors:

```python
>>> 8 + 9 -
SyntaxError: invalid syntax
```

---

## Strings

A **string** is a sequence of characters. Strings can be enclosed in single quotes `'...'`, double quotes `"..."`, or triple quotes for multi-line strings `'''...'''` or `"""..."""`.

### Single and double quotes

Both are equivalent, choose whichever avoids the need to escape characters.

```python
>>> print('navin')
navin
>>> print("navin")
navin
```

### Using quotes inside strings

* If the string contains an apostrophe, use double quotes outside to avoid escaping.

```python
>>> print("navin's laptop")
navin's laptop
```

* If you must use the same quote inside and outside, escape the inner quote with a backslash `\`.

```python
>>> print('navin\'s "laptop"')
navin's "laptop"
```

### Triple-quoted strings (multi-line)

```python
text = '''This is a
multi-line string.'''
print(text)
```

### Escaping special characters

The backslash `\` introduces escape sequences like `\n` (newline), `\\` (a literal backslash), `\t` (tab), etc.

```python
>>> print('Line1\nLine2')
Line1
Line2
```

**Common error**: mismatched quotes cause `SyntaxError`:

```python
>>> print('navin's laptop')
SyntaxError: invalid syntax
```

---

## Functions

A function is a block of organized, reusable code that performs a specific task. Python has many built-in functions (e.g., `print()`, `len()`) and you can define your own, which we will discuss in more detail later in the course.

### Built-in function example

```python
>>> len('hello')
5
>>> print('Hello, world!')
Hello, world!
```

## Concatenation and Repetition of strings

### Concatenation using `+`

Joins two strings into one. Both operands must be strings.

```python
>>> 'navin' + ' reddy'
'navin reddy'
```

### Repetition using `*`

Repeats a string multiple times.

```python
>>> 'navin ' * 3
'navin navin navin '
```

**Type error example**:

```python
>>> 'navin' + 5
TypeError: can only concatenate str (not "int") to str
```

---

## 6. New line character and raw strings

### `\n` — newline character

`\n` in a string inserts a newline when printed.

```python
>>> print('c:\\docs\navin')
c:\docs
avin
```

### Raw strings `r'...'`

Raw strings treat backslashes `\\` as literal characters. Useful for file paths or regular expressions.

```python
>>> print(r'c:\docs\navin')
c:\docs\navin
```

> **Note:** A raw string cannot end with a single backslash (`r"something\"` is invalid). Use normal strings or escape the final backslash.

