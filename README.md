
---

### 📌 1. Print numbers from 1 to N using recursion

```python
def print_1_to_n(n):
    if n == 0:
        return
    print_1_to_n(n - 1)
    print(n)

print_1_to_n(5)
```

**Output:**

```
1
2
3
4
5
```

---

### 📌 2. Print numbers from N to 1 using recursion

```python
def print_n_to_1(n):
    if n == 0:
        return
    print(n)
    print_n_to_1(n - 1)

print_n_to_1(5)
```

**Output:**

```
5
4
3
2
1
```

---

### 📌 3. Print even numbers from 1 to N using recursion

```python
def print_even(n):
    if n == 0:
        return
    print_even(n - 1)
    if n % 2 == 0:
        print(n)

print_even(10)
```

**Output:**

```
2
4
6
8
10
```

---

### 📌 4. Sum of first N natural numbers using recursion

```python
def sum_n(n):
    if n == 0:
        return 0
    return n + sum_n(n - 1)

print(sum_n(5))
```

**Output:**

```
15
```

---

### 📌 5. Factorial of a number using recursion

```python
def factorial(n):
    if n == 0 or n == 1:
        return 1
    return n * factorial(n - 1)

print(factorial(5))
```

**Output:**

```
120
```

---

### 📌 6. Power of a number (a^b) using recursion

```python
def power(a, b):
    if b == 0:
        return 1
    return a * power(a, b - 1)

print(power(2, 3))
```

**Output:**

```
8
```

---

### 📌 7. Fibonacci number at position N using recursion

```python
def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n - 1) + fibonacci(n - 2)

print(fibonacci(6))
```

**Output:**

```
8
```

---

### 📌 8. Check if a string is a palindrome using recursion

```python
def is_palindrome(s):
    if len(s) <= 1:
        return True
    if s[0] != s[-1]:
        return False
    return is_palindrome(s[1:-1])

print(is_palindrome("121"))
```

**Output:**

```
True
```

---

### 📌 9. Find sum of digits of a number using recursion

```python
def sum_of_digits(n):
    if n == 0:
        return 0
    return n % 10 + sum_of_digits(n // 10)

print(sum_of_digits(1234))
```

**Output:**

```
10
```

---

### 📌 10. Count digits of a number using recursion

```python
def count_digits(n):
    if n == 0:
        return 0
    return 1 + count_digits(n // 10)

print(count_digits(1234))
```

**Output:**

```
4
```

---


