# Operators — Complete Guide

**Date:** 2026-08-05

## 1. Arithmetic operators
| Operator | Meaning | Example |
|----------|---------|---------|
| `+` | Addition | `5 + 2` → `7` |
| `-` | Subtraction | `5 - 2` → `3` |
| `*` | Multiplication | `5 * 2` → `10` |
| `/` | Division (always float) | `5 / 2` → `2.5` |
| `//` | Floor division | `5 // 2` → `2` |
| `%` | Modulus (remainder) | `5 % 2` → `1` |
| `**` | Exponent | `5 ** 2` → `25` |

## 2. Comparison operators
Return `True`/`False`: `==`, `!=`, `>`, `<`, `>=`, `<=`

## 3. Logical operators
| Operator | Meaning |
|----------|---------|
| `and` | True if both sides are True |
| `or` | True if at least one side is True |
| `not` | Inverts the boolean |

## 4. Assignment operators
`=`, `+=`, `-=`, `*=`, `/=`, `//=`, `%=`, `**=` — shorthand for updating a variable based on its current value.

```python
count = 0
count += 1   # same as count = count + 1
```

## 5. Membership operators
`in` and `not in` — check if a value exists inside a sequence.
```python
"a" in "apple"        # True
5 not in [1, 2, 3]    # True
```

## 6. Identity operators
`is` and `is not` — check if two variables point to the **same object** in memory, not just an equal value.

## 7. Bitwise operators (advanced)
Operate on the binary representation of integers.

| Operator | Meaning | Example |
|----------|---------|---------|
| `&` | AND | `5 & 3` → `1` |
| `\|` | OR | `5 \| 3` → `7` |
| `^` | XOR | `5 ^ 3` → `6` |
| `~` | NOT (inverts bits) | `~5` → `-6` |
| `<<` | Left shift | `5 << 1` → `10` |
| `>>` | Right shift | `5 >> 1` → `2` |

Bitwise operators are rare in everyday data science code but show up in low-level optimizations, hashing, and flags.

## 8. Operator precedence (advanced)
Python evaluates in this general order (high → low):
`()` → `**` → unary `+x/-x` → `* / // %` → `+ -` → bitwise → comparisons → `not` → `and` → `or`

When in doubt, use parentheses — precedence bugs are hard to spot in review.

## 9. Chained comparisons (advanced)
Python lets you chain comparisons naturally, unlike many languages:
```python
x = 5
print(1 < x < 10)   # True — equivalent to (1 < x) and (x < 10)
```

## 10. Ternary (conditional) operator (advanced)
A one-line if/else expression:
```python
age = 20
status = "adult" if age >= 18 else "minor"
```

## 11. Walrus operator `:=` (advanced, Python 3.8+)
Assigns a value as part of an expression — useful for avoiding repeated computation.
```python
data = [1, 2, 3, 4, 5]
if (n := len(data)) > 3:
    print(f"List has {n} items, which is more than 3")
```

## 12. Operator overloading (preview, advanced)
Custom objects can define what `+`, `==`, etc. mean for them via dunder methods (`__add__`, `__eq__`). Covered properly once we reach OOP — mentioned here just so the term isn't a surprise later.

## Key takeaways
- `/` vs `//` and `==` vs `=` and `is` vs `==` are the three most common beginner mix-ups
- Bitwise, walrus, and chained comparisons are "advanced" mostly because they're less common, not because they're hard
- When precedence isn't obvious at a glance, add parentheses — it costs nothing and prevents bugs
