
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

## ✅ Array-based Recursion Problems

### 1. Check if an array is sorted using recursion

```python
def is_sorted(arr, index=0):
    if index == len(arr) - 1:
        return True
    return arr[index] <= arr[index + 1] and is_sorted(arr, index + 1)

print(is_sorted([1, 2, 3, 4]))   # Output: True
print(is_sorted([5, 3, 2]))      # Output: False
```

---

### 2. Find the maximum element in an array using recursion

```python
def find_max(arr, index=0):
    if index == len(arr) - 1:
        return arr[index]
    return max(arr[index], find_max(arr, index + 1))

print(find_max([3, 5, 1, 9, 6]))   # Output: 9
```

---

### 3. Find the first index of a given element in array

```python
def first_index(arr, x, index=0):
    if index == len(arr):
        return -1
    if arr[index] == x:
        return index
    return first_index(arr, x, index + 1)

print(first_index([4, 2, 7, 7, 5], 7))  # Output: 2
```

---

### 4. Find the last index of a given element in array

```python
def last_index(arr, x, index=0):
    if index == len(arr):
        return -1
    res = last_index(arr, x, index + 1)
    if res != -1:
        return res
    if arr[index] == x:
        return index
    return -1

print(last_index([4, 2, 7, 7, 5], 7))  # Output: 3
```

---

### 5. Search for an element in an array (linear search using recursion)

```python
def linear_search(arr, x, index=0):
    if index == len(arr):
        return False
    if arr[index] == x:
        return True
    return linear_search(arr, x, index + 1)

print(linear_search([1, 4, 6, 9], 6))   # Output: True
print(linear_search([1, 4, 6, 9], 2))   # Output: False
```

---

## ✅ String and Pattern Problems

### 6. Reverse a string using recursion

```python
def reverse_string(s):
    if len(s) == 0:
        return ""
    return reverse_string(s[1:]) + s[0]

print(reverse_string("hello"))  # Output: "olleh"
```

---

### 7. Check if a string is palindrome using recursion

```python
def is_palindrome(s):
    if len(s) <= 1:
        return True
    if s[0] != s[-1]:
        return False
    return is_palindrome(s[1:-1])

print(is_palindrome("madam"))  # Output: True
print(is_palindrome("apple"))  # Output: False
```

---

### 8. Replace all occurrences of 'a' with 'b' in a string using recursion

```python
def replace_a_with_b(s):
    if len(s) == 0:
        return ""
    if s[0] == 'a':
        return 'b' + replace_a_with_b(s[1:])
    return s[0] + replace_a_with_b(s[1:])

print(replace_a_with_b("apple and banana"))  # Output: "bpple bnd bbnbnb"
```

---

### 9. Remove duplicates from a string using recursion

```python
def remove_duplicates(s, seen=set()):
    if not s:
        return ""
    if s[0] in seen:
        return remove_duplicates(s[1:], seen)
    seen.add(s[0])
    return s[0] + remove_duplicates(s[1:], seen)

print(remove_duplicates("aabbccdde"))  # Output: "abcde"
```

---

### 10. Count the number of vowels in a string using recursion

```python
def count_vowels(s):
    if not s:
        return 0
    return (s[0].lower() in 'aeiou') + count_vowels(s[1:])

print(count_vowels("Recursion is powerful"))  # Output: 8
```

---
