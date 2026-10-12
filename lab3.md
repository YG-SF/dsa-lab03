# Lab 3

## Part A - Recursive Analysis

Use the course resource on recursive-function analysis:

https://seneca-ictoer.github.io/data-structures-and-algorithms/C-Recursion/analysis-of-recursive-functions

Complete your analysis for each required function below. Analyze the code exactly as provided.

### Function 1

Analyze the following function with respect to `n`.

```python
def function1(value, n):
    if n == 0:
        return 1
    elif n == 1:
        return value
    else:
        return value * function1(value, n - 1)
```

### Your analysis

Write your complete analysis here.

---

### Function 2

Analyze `recursive_function2` with respect to the length of `my_string`.

```python
def recursive_function2(my_string, a, b):
    if a >= b:
        return True
    else:
        if my_string[a] != my_string[b]:
            return False
        else:
            return recursive_function2(my_string, a + 1, b - 1)


def function2(my_string):
    return recursive_function2(my_string, 0, len(my_string) - 1)
```

### Your analysis

Write your complete analysis here.

---

### Function 3

Analyze the following function with respect to `n`.

```python
def function3(value, n):
    if n == 0:
        return 1
    elif n == 1:
        return value
    else:
        half = n // 2
        result = function3(value, half)

        if n % 2 == 0:
            return result * result
        else:
            return value * result * result
```

### Your analysis

Write your complete analysis here.

## Part C - Reflection

Answer the following questions:

1. Describe your approach to writing a recursive function. What steps do you normally take?
2. Describe the process of analyzing recursive functions. How does it differ from analyzing non-recursive functions? How is it similar?
3. What did you learn while implementing the doubly linked list? What approach did you take, and which bugs or pointer/reference issues were the most difficult to fix?
