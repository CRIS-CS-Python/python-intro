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

* the `>>>` prompt is not displayed preceeding expressions.
* a `#> ` comment is displayed *before* the output value.

To lauch the Python 3 shell:

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

## References

1. [Python.org - Builtin Types](https://docs.python.org/3/library/stdtypes.html)
2. [RealPython - Basic Data Types](https://realpython.com/python-data-types/)
