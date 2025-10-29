# 25. Prime Number in Python


In this lecture, we will learn how to check whether a given number is prime or not using different approaches, from the basic method to more efficient algorithms.


## Prime Number

A **prime number** is a **positive integer greater than 1** that has **no divisors other than 1 and itself**.
In simple terms, it cannot be formed by multiplying two smaller natural numbers.

### Examples of Prime Numbers:

```
2, 3, 5, 7, 11, 13, 17, 19, 23, ...
```

### Note:

* `1` is **not a prime number**, as it has only one divisor (1 itself).
* `2` is the **smallest prime number** and also the **only even prime number**.
* There are **infinitely many** prime numbers.


---


## Understanding the Concept

Let’s visualize the idea of checking whether a number `n` is prime.

```
Divisibility Check
--------------------------------
1     2     3     4     5     6
|           |
✔           ❌
Only divisible by 1 and itself → PRIME
```

To determine if a number is prime:

1. Try dividing it by numbers from **2** up to **n-1**.
2. If any number divides it evenly, it’s **not prime**.
3. If no divisors are found, it’s **prime**.


---


## 1. Basic Approach: Check Divisibility from 2 to n−1

```python
num = int(input("Enter a number: "))

for i in range(2, num):
    if num % i == 0:
        print("Not Prime")
        break
else:
    print("Prime")
```

### **Example Input/Output:**

```
Enter a number: 7
Prime

Enter a number: 8
Not Prime
```

### **Explanation:**

* The loop checks divisibility from 2 to `num-1`.
* If any number divides evenly (`num % i == 0`), the loop breaks → `Not Prime`.
* If no divisors are found, the `else` block executes → `Prime`.

**Advantage:** Simple and easy to understand.

**Limitation:** Inefficient for large numbers (checks too many unnecessary values).


---


## 2. Improved Approach: Check Up to Half the Number

We can optimize the previous code by checking divisors only up to **half of the number** (`num // 2`).
Any number greater than `num // 2` cannot divide `num` evenly (except `num` itself).

```python
num = int(input("Enter a number: "))

for i in range(2, num // 2):
    if num % i == 0:
        print("Not Prime")
        break
else:
    print("Prime")
```

### **Example Input/Output:**

```
Enter a number: 13
Prime

Enter a number: 20
Not Prime
```

**Advantage:** Fewer iterations → faster than the previous approach.

**Limitation:** Still inefficient for very large numbers.


---


## 3. Most Efficient Approach: Check Up to √n (Square Root Method)

We can optimize even further using a **mathematical insight**:

> If a number `n` is divisible by any number greater than √n, then it must have a smaller divisor less than √n.
Hence, it’s enough to check divisibility only up to `√n`.


### **Optimized Code Using `math.sqrt()`**

```python
import math

n = int(input("Enter a number: "))

if n <= 1:
    print("Not Prime")
elif n <= 3:
    print("Prime")
elif n % 2 == 0 or n % 3 == 0:
    print("Not Prime")
else:
    for i in range(5, int(math.sqrt(n)) + 1, 6):
        if n % i == 0 or n % (i + 2) == 0:
            print("Not Prime")
            break
    else:
        print("Prime")
```

### **Example Input/Output:**

```
Enter a number: 19
Prime

Enter a number: 21
Not Prime
```

---


## Performance Comparison

| Approach    | Range Checked | Time Complexity | Efficiency |
| ----------- | ------------- | --------------- | ---------- |
| Basic       | 2 → n−1       | O(n)            | Slow       |
| Half-Range  | 2 → n/2       | O(n/2)          | Better     |
| Square Root | 2 → √n        | O(√n)           | Best       |


---


## Key Takeaways

* A prime number has exactly two distinct factors: `1` and the number itself.
* Use the `for-else` structure to neatly handle prime detection.
* Checking only up to **√n** makes the program highly efficient.
* Always handle edge cases (`n ≤ 1`, `n = 2`, `n = 3`) separately.
* This concept is foundational for advanced topics like:
  - Cryptography
  - Prime factorization
  - Number theory algorithms


