# ![Chiang Rai International School](../images/logo.png?raw=true) Introduction to Python

## Booleans

A *boolean expression* evaluates to either a value of `True` or `False`.

### Boolean Operators

* `and`
* `or`
* `not`

### Logical Comparisons (Produces a Boolean Value)

| Operator | Meaning                  |
|----------|--------------------------|
| <        | Less than                |
| <=       | Less than or equal to    |
| >        | Greater than             |
| >=       | Greater than or equal to |
| ==       | is equal to              |
| !=       | is *not* equal to        |

Watch the [AC 101 Boolean Logic](https://www.youtube.com/watch?v=Y6CwThhquQs) lesson to
see how these expressions are evaluated.

## Conditionals

A conditional statement, such as a `if` or `while` statement, will evaluate a block of code based
on the `True` or `False` value of a boolean expression.

### Nested Conditional Example

A conditional can occur inside another conditional, called a *nested condition*.

This is an example of nested `if` statements.

```python
gender = "F"
age = 15

# print Man, Woman, Boy, Girl or Unknown given gender and age
if gender.lower() in ("male", "m"):
    if age >= 18:
        print("Man")
    else:
        print("Boy")
elif gender.lower() in ("female", "f"):
    if age >= 18:
        print("Woman")
    else:
        print("Girl")
else:
    print(f"Unknown gender: {gender}")
```

Study the code above and understand why the following values for `gender` and `age`
produce the different output.

| `gender`   | `age` | Output              |
|------------|-------|---------------------|
| `"Male"`   | `18`  | Man                 |
| `"Male"`   | `12`  | Boy                 |
| `"Female"` | `32`  | Woman               |
| `"Female"` | `7`   | Girl                |
| `"???"`    |       | Unknown gender: ??? |

## References

1. [Python.org: Compound Statements](https://docs.python.org/3/reference/compound_stmts.html)
2. [Corey Schafer - Python Conditionals](https://www.youtube.com/watch?v=daefaLgNkw0&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU&index=6)
3. [Google Students AC101 - Boolean Logic](https://www.youtube.com/watch?v=Y6CwThhquQs)
4. [Google Students AC101 - Conditionals](https://www.youtube.com/watch?v=OQ8uakCJ6yE)
