# For Loop in Python


## Understanding Loops in Python

Loops are used in programming to **execute a block of code multiple times**.  
Python provides two main types of loops:

1. **while loop** – Repeats a block of code as long as a specified condition is `True`.  
2. **for loop** – Iterates over a sequence (like list, tuple, string, or range).


---


## Difference Between While and For Loops

| **Feature** | **while loop** | **for loop** |
|--------------|----------------|---------------|
| **Condition** | Requires a condition to be `True` | Works with an iterable object |
| **Use Case** | When the number of iterations is not known in advance | When iterating over sequences or a known range |
| **Control Variable** | Must be manually initialized and updated | Automatically updated by the loop |


---


## 3. The For Loop

In Python, a `for` loop is used to **iterate over a sequence of elements** such as a list, tuple, dictionary, set, or string.

### Syntax:
```python
for variable in sequence:
    # Code to be executed in each iteration
```

Each time the loop runs, the variable takes the next value from the sequence until all items are processed.


---

## Examples of Foor Loop
### 1. Iterating Through a List
```python
x = ['Navin', 65, 2.5]
for i in x:
    print(i)
```
**Output:**
```
Navin
65
2.5
```


### 2. Iterating Through a String
```python
x = 'NAVIN'
for i in x:
    print(i)
```
**Output:**
```
N
A
V
I
N
```


### 3. Iterating Through a List Literal
```python
for i in [2, 6, 'Muskan']:
    print(i)
```
**Output:**
```
2
6
Muskan
```

---


##  Using the `range()` Function

The `range()` function generates a sequence of numbers, which can be used with `for` loops.

### Example 1: Default range (0 to 9)
```python
for i in range(10):
    print(i)
```
**Output:**
```
0
1
2
3
4
5
6
7
8
9
```

### Example 2: Range with Start, Stop, and Step
```python
for i in range(11, 21, 1):
    print(i)
```
**Output:**
```
11
12
13
14
15
16
17
18
19
20
```

### Example 3: No Output Case
```python
for i in range(20, 11):
    print(i)
```
Since the default step is `+1`, and the start is greater than the stop value, **no output** will be produced.


---


## Reversing the Range
You can reverse the range using a **negative step value**:
```python
for i in range(20, 10, -1):
    print(i)
```
**Output:**
```
20
19
18
17
16
15
14
13
12
11
```


---


## Using Conditions with For Loop

You can add conditions inside the `for` loop to control which items are processed.

### Example 1: Skip Numbers Divisible by 5
```python
for i in range(1, 21):
    if i % 5 == 0:
        pass
    else:
        print(i)
```
**Output:**
```
1
2
3
4
6
7
8
9
11
12
13
14
16
17
18
19
```

### Example 2: Print Only Numbers Not Divisible by 5
```python
for i in range(1, 21):
    if i % 5 != 0:
        print(i)
```
**Output:**
```
1
2
3
4
6
7
8
9
11
12
13
14
16
17
18
19
```


---


## Summary

| **Concept** | **Explanation** |
|--------------|----------------|
| `for` loop | Used to iterate through sequences |
| `range()` | Generates a sequence of numbers |
| `pass` | Skips execution of that iteration |
| `if` condition | Used to control which elements are processed |
| **Step** | Controls how much the loop variable changes after each iteration |


