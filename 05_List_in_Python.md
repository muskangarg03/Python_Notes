# List in Python
A list in Python is a collection used to store multiple items in a single variable.
- Lists are **mutable**, their elements can be modified after creation.
- Lists are defined using square brackets [ ], and values are separated by commas.
- Lists can hold different data types: integers, floats, strings, or even other lists.


## Creating a List
**Example:**

```python
nums = [25, 12, 36, 95, 14]
print(nums)   # [25, 12, 36, 95, 14]
```

### Accessing Elements:
- List elements can be accessed using indexing (index starts at 0).
- If the list size is `n`, valid index values range from `0` to `n-1`.
- Negative indexing is also allowed (just like strings).

```python
print(nums[0])   # 25
print(nums[4])   # 14
print(nums[-1])  # 14
print(nums[-5])  # 25
```

> If an index is out of range, Python raises an IndexError:
```python
print(nums[54])  
# IndexError: list index out of range
```

### Slicing a List:
```python
print(nums[2:])    # [36, 95, 14]
print(nums[:3])    # [25, 12, 36]
```

---


## Different Types of Lists

### 1. List of String
```python
print(nums[2:])    # [36, 95, 14]
print(nums[:3])    # [25, 12, 36]
```

### 2. List of Mixed Data Types
```python
values = [9.5, 'Navin', 25]
print(values)   # [9.5, 'Navin', 25]
```


### 3. List of Lists (Nested Lists)
```python
mil = [nums, names]
print(mil)  
# [[25, 12, 36, 95, 14], ['navin', 'kiran', 'john']]
```

---


## List Methods and Operations

### (a) Adding Elements

- **append()** → adds a single value to the end of the list.
```python
nums.append(45)
print(nums)   # [25, 12, 36, 95, 14, 45]
```

- **insert(index, value)** → inserts a value at a specific position.
```python
nums.insert(2, 77)
print(nums)   # [25, 12, 77, 36, 95, 14, 45]
```

- **extend(list)** → adds multiple values at once.
```python
nums.extend([29, 12, 14, 36])
print(nums)   # [25, 12, 77, 36, 95, 14, 45, 29, 12, 14, 36]
```


### (b) Removing Elements
- **remove(value)** → removes the first occurrence of a value.
```python
nums.remove(14)
print(nums)   # [25, 12, 77, 36, 95, 45]

```

- **pop(index)** → removes element at the given index and returns it.
```python
nums.pop(1)    # returns 12
print(nums)    # [25, 77, 36, 95, 45]

```

- **pop()** without index → removes and returns the last element.
```python
nums.pop()     # returns 45

```

- **del list[start:end]** → deletes a sublist.
```python
del nums[2:]
print(nums)    # [25, 77]

```

- **clear()** → removes all elements from the list.
```python
nums.clear()
print(nums)   # []
```


### (c) Sorting and Ordering
- **sort()** → sorts the list in ascending order.
```python
nums = [25, 77, 29, 12, 14, 36]
nums.sort()
print(nums)   # [12, 14, 25, 29, 36, 77]
```

---

## Built-in Functions with Lists
- **min(list)** → returns the smallest element.
```python
min(nums)   # 12
```

- **maxlist)** → returns the largest element.
```python
max(nums)   # 77
```

- **sum(list)** → returns the sum of all elements.
```python
sum(nums)   # 193
```
