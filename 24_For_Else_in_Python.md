
# 24. For-Else in Python


## Introduction to For-Else Loop

A **`for-else` loop** allows you to execute an **`else` block** of code after the `for` loop **completes all its iterations normally**, i.e., **without encountering a `break` statement**.

If the loop is **terminated early** using `break`, the `else` block **will not execute**.


### **Basic Syntax**

```python
for item in sequence:
    # loop body
else:
    # else block
```

* **`sequence`** → any iterable object such as a list, tuple, string, or range.
* The `for` loop runs once for each item in the sequence.
* When the loop finishes all iterations normally, the `else` block runs.
* If a `break` statement is executed during the loop, the `else` block is **skipped**.


---


## Understanding the Flow

| Step                       | Condition            | Result                    |
| -------------------------- | -------------------- | ------------------------- |
| The loop executes normally | No `break` occurs    | `else` block **executes** |
| The loop ends early        | `break` is triggered | `else` block **skipped**  |


---


## Example 1: Without `for-else` (Printing "Not Found" every time)

Suppose we want to find the **first number divisible by 5** in a list.
If the number is not divisible by 5, we print `"not found"` every time.

```python
nums = [12, 15, 18, 21, 26]

for num in nums:
    if num % 5 == 0:
        print(num)
        break
    else:
        print("not found")
```

### **Output:**

```
not found
15
```

**Explanation:**

* The loop checks each number.
* For `12`, the condition `num % 5 == 0` is false, so it prints `"not found"`.
* When it reaches `15`, the condition is true → it prints `15` and executes `break`.
* The loop stops immediately after finding the first match.

> This approach prints `"not found"` **for every non-matching number**, which can be repetitive and unnecessary.


---


## Example 2: Using `for-else` (Printing “Not Found” Once)

The **`for-else`** structure provides a cleaner way to handle the same logic, it allows you to print `"not found"` **only once**, if no element satisfies the condition.

```python
nums = [23, 24, 27, 38, 29]

for num in nums:
    if num % 5 == 0:
        print(num)
        break
else:
    print("not found")
```

### **Output:**

```
not found
```

**Explanation:**

* The loop iterates through each number.
* No number is divisible by 5, so `break` never executes.
* Since the loop completed normally, the `else` block runs and prints `"not found"`.

Now, let’s modify the list to include a number divisible by 5:

```python
nums = [23, 25, 27, 38, 29]

for num in nums:
    if num % 5 == 0:
        print(num)
        break
else:
    print("not found")
```

### **Output:**

```
25
```

**Explanation:**

* When the loop finds `25`, it prints the number and executes `break`.
* The loop terminates early, so the `else` block is **skipped**.


---


## Practical Uses of `for-else`

* Searching for an element in a list or sequence.
* Validating conditions in loops.
* Running a fallback or final action if no `break` occurs.
* Performing cleanup operations after a loop finishes.


---


## Key Takeaways

* The `for-else` loop is a powerful Python construct often used for searching and validation tasks.
* The `else` block runs only when the loop finishes without hitting a `break`.
* If a `break` occurs, the `else` block is skipped.
* It provides a cleaner, more Pythonic alternative to using flags or repeated conditions.
