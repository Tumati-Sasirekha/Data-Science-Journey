# Data Types



## Python's built-in data types

| Type | Example | Description |
|------|---------|-------------|
| `int` | `42` | Whole numbers |
| `float` | `3.14` | Decimal numbers |
| `str` | `"hello"` | Text |
| `bool` | `True` / `False` | Boolean values |
| `list` | `[1, 2, 3]` | Ordered, mutable collection |
| `tuple` | `(1, 2, 3)` | Ordered, immutable collection |
| `dict` | `{"key": "value"}` | Key-value pairs |
| `set` | `{1, 2, 3}` | Unordered collection of unique items |
| `NoneType` | `None` | Represents "no value" |

## Checking a type
```python
x = 10
print(type(x))   # <class 'int'>
```

## Type casting
```python
int("5")      # 5
str(5)        # "5"
float("3.14") # 3.14
bool(0)       # False
bool(1)       # True
```

## Mutable vs immutable
- **Mutable** (can change after creation): `list`, `dict`, `set`
- **Immutable** (cannot change after creation): `int`, `float`, `str`, `tuple`, `bool`

## Key takeaways
- Every value in Python has a type, even if you didn't declare one
- Mutability matters — it affects how variables behave when passed around or copied
- Type casting is common when reading input (which always comes in as a string)


