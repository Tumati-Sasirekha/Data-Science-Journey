# Reading User Input

**Date:** 2026-08-05

## The basics
`input()` always returns a **string**, no matter what the user types.

```python
value = input("Enter something: ")
print(type(value))   # always <class 'str'>
```

## Converting input to other types
Since `input()` returns a string, you cast it to whatever type you actually need.

```python
age = int(input("Enter your age: "))
price = float(input("Enter price: "))
```

## Reading multiple values on one line
Use `.split()` to break the input into pieces, then convert each.

```python
a, b = input("Enter two numbers separated by space: ").split()
a, b = int(a), int(b)
```

A common one-liner using `map()`:
```python
a, b = map(int, input("Enter two numbers: ").split())
```

## Reading a list of values
```python
nums = list(map(int, input("Enter numbers separated by space: ").split()))
```

## Handling invalid input safely
If the user types something that can't convert, `int()`/`float()` raise a `ValueError`. Wrap conversions in `try/except` to handle this gracefully.

```python
try:
    age = int(input("Enter your age: "))
except ValueError:
    print("That's not a valid number.")
```

## Reading boolean-like input
There's no built-in `bool(input(...))` cast that works the way you'd expect — `bool("False")` is actually `True` (any non-empty string is truthy). Compare the string manually instead.

```python
answer = input("Continue? (yes/no): ").strip().lower()
is_yes = answer == "yes"
```

## Key takeaways
- `input()` output is always `str` — cast it explicitly to `int`, `float`, etc.
- `.split()` + unpacking or `map()` handles multiple values on one line
- Never assume input is valid — wrap type conversions in `try/except`
- Checking booleans from input needs a string comparison, not `bool()`

