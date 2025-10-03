# ![Chiang Rai International School](../images/logo.png?raw=true) Introduction to Python

## Python Basic Types

| Class            | Type                   |
|------------------|------------------------|
| int              | Integer numbers        |
| float            | Floating-point numbers |
| complex          | Complex numbers        |
| str              | Strings and characters |
| bytes, bytearray | Bytes                  |
| bool             | Boolean values         |

### Code Examples

The code examples are meant to be run in the Python 3 interactive shell (REPL).

However,

* the `>>>` prompt is not displayed preceding expressions.
* a `#> ` comment is displayed *before* the output value.

To launch the Python 3 shell:

#### Windows Users

```bash
py -i
```

#### *NIX Users (Mac, Linux, etc...)

```bash
python3 -i
```

### Comments

"A [comment](https://en.wikipedia.org/wiki/Comment_(computer_programming)#Python) is a human-readable explanation or annotation in the source code of a computer program."

They are ignored by the Python interpreter.

```python
# This is a comment
# Text after a '#' character is ignored by the Python interpreter
print("This is interpreted code")  # but comments can also come after code on the same line
```

### Numeric Types

#### Integers

This code will show the type of a *literal* `37`. Its called a literal because the value *is what it is*, not a variable or compound expression that can also have the same type.

```python
type(37)
#> <class 'int'>
```

#### Floats

A floating point number is a rational number, however we use the term *floating point*
instead of *decimal point* to avoid confusion with the term "decimal numbers" which
indicates a *base 10* number in Computer Science.

```python
type(21.7)
#> <class 'float'>
```

##### Division

Note that division (`/`) produces floats even for *whole numbers*.

```python
21/1
#> 21.0

type(21/1)
#> <class 'float'>
```

##### Integer Division

Use (`//`) for integer division.

```python
21//1
#> 21

type(21//1)
#> <class 'int'>
```

### Strings

"Textual data in Python is handled with `str` objects, or strings. Strings are immutable sequences of Unicode code points."[1]

[*Characters*](https://en.wikipedia.org/wiki/Character_(computing)) in *string literals* must be enclosed in single or double quotes.

Examples:

```python
'This is a literal string'
```

```python
"This is also a literal string"
```

However, single or double quotes must be used consistently.

```python
"This is not a string literal, but a syntax error :('
```

*Docstrings* can span multiple lines, enclosed by three (single or double) quotes.

```python
'''This is
a multiline
string literal'''
```

```python
type("Hello World")
#> <class 'str'>
```

### Booleans

A *boolean* type has a value of either `True` or `False`.

Note that bare values `true` or `false` (all lowercase and not enclosed in quotes) are
treated as if they are variable names and would result in `NameError`s.

However, most other types can be deduced as a boolean in [*logical expressions*](https://realpython.com/python-operators-expressions/#boolean-operators-and-expressions-in-python) or by using the `bool()` function.

```python
type(True)
#> <class 'bool'>

type(False)
#> <class 'bool'>

# "empty" values are deduced as False, everything else True
bool(1)
#> True
bool(27.1)
#> True
bool(0)
#> False
bool(0.0)
#> False
bool("")  # empty string
#> False
bool(" ") # string containing a single space
#> True
```

## Variables

In computer science, a **variable** is a name that refers to a **value** stored in memory.

### Example (C-style visualization)

Python is written in the **C programming language**, so let's visualize declaring an `int` variable and **assigning** it a value.

This is C code, so it won't work in the Python interpreter. But, for example, suppose we write:

```c
/* declare a variable `x` of type `int` with a value `27` */
int x = 27;
```

We can visualize it like this:

| Variable Name | Memory Address | Value |
|---------------|----------------|-------|
| `x`           | `0x7ffee3b4`   | `27`  |

* `x` is the **variable name**.
* `0x7ffee3b4` is the **address in RAM** where the value is stored.
* The storage location at that address contains the **integer value 27** (but as a **binary number**).

---

## Python Example

Python is **dynamically typed**, so we don't have to declare the type of a
variable like in the C language (or other *strongly-typed* languages like C++, or Java).

This means that the type is **inferred** by its value.

```python
x = 27
y = x
```

Visualization (simplified):

| Variable Name | Memory Address (of object) | Value |
|---------------|----------------------------|-------|
| `x`           | `0x1001`                   | `27`  |
| `y`           | `0x1001`                   | `27`  |

Both `x` and `y` point to the **same object** in memory.

Changing the value of `x` by *rebinding* (e.g., `x = 42`) doesn’t change `y`. Instead, `x` now points to a different object.

```python
# `x` contains a value `27`, now update it to `42`
x = 42
```

Visualization (simplified):

| Variable Name | Memory Address (of object) | Value |
|---------------|----------------------------|-------|
| `y`           | `0x1002`                   | `27`  |
| `x`           | `0x1002`                   | `42`  |

A **variable is not the value itself** — it’s a name (label) that points to a
location where the value is stored in memory.

## References

1. [Python.org - Builtin Types](https://docs.python.org/3/library/stdtypes.html)
2. [RealPython - Basic Data Types](https://realpython.com/python-data-types/)
