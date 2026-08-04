# Variables

## What is a variable?
A variable is a name that refers to a value stored in memory. In Python you don't declare a type up front — the type is inferred automatically from whatever value you assign.

```python
name = "Alice"
age = 25
height = 5.6
```

## Naming rules
- Must start with a letter or underscore (not a digit)
- Can contain letters, digits, and underscores
- Case-sensitive (`age` and `Age` are different variables)
- Can't use reserved keywords (`for`, `if`, `class`, etc.)
- Convention: use `snake_case` for variable names

## Reassignment and dynamic typing
A variable can be reassigned to a completely different type at any point:

```python
x = 10          # x is an int
x = "hello"     # now x is a str
```

## Multiple assignment
Python lets you assign several variables in one line:

```python
a, b, c = 1, 2, 3
```

## Key takeaways
- Variables are just labels pointing to values — not fixed containers
- No type declaration needed; Python infers it at runtime
- Naming clearly matters more as code grows — future-me will thank present-me

