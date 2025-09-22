# Tuple and Set in Python


## 1. Tuples

A **tuple** is an ordered collection of elements, similar to a list, but unlike lists, tuples are **immutable**, meaning their values cannot be changed after creation.  

**Creating a Tuple:**  

```python
tup = (21, 36, 14, 25)
print(tup)
# Output: (21, 36, 14, 25)
```

**Accessing Elements:**

```python
print(tup[1])
# Output: 36
```

**Immutability:**

```python
tup[1] = 33
# TypeError: 'tuple' object does not support item assignment
```

**Tuple Method (count):**

**`count(element)`** – Returns the number of occurrences of an element in the tuple.

```python
tup = (5, 2, 5, 7)
print(tup.count(5))
# Output: 2
```

### Iteration
Iterating over tuples is faster than lists, making them suitable for scenarios where performance is critical and data should remain constant.

### When to use Tuples
- When you need an ordered collection of elements that should not be changed.
- When iteration speed is important, as tuples are more efficient than lists.


---


## 2. Sets
A **set** is a collection of **unique elements** that is **unordered**. Sets do not allow duplicates and do not maintain the sequence of elements.

**Creating a Set:**  

```python
s = {22, 25, 14, 21, 5}
print(s)
# Output: {5, 21, 22, 25, 14}  # Order may vary
```

**Duplicate Elements:**
```python
s = {25, 14, 98, 63, 75, 98}
print(s)
# Output: {98, 25, 75, 14, 63}
```

### Properties of Sets
- **Unordered:** Elements do not maintain the sequence.
- **Unique Elements:** No duplicates allowed.
- **Indexing Not Supported:**
```python
s[2]
# TypeError: 'set' object is not subscriptable
```
- **Hash-Based:** Sets use hashing for fast access and efficient performance.
- **Mutability:** While the set itself is mutable (you can add or remove elements), you cannot change a specific element because there is no indexing.

### When to use Sets
- When you need a collection of unique elements.
- When the order of elements does not matter.
