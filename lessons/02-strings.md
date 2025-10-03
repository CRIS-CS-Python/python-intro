# ![Chiang Rai International School](../images/logo.png?raw=true) Introduction to Python

"Textual data in Python is handled with `str` objects, or strings. Strings are immutable sequences of Unicode code points."[1]

## String Concatenation

Concatenate means to join two or more things together, like adding additional links to a chain.

The `+` operator after a string indicates *string concatenation*, not addition.

```python
"Hello World"
#> Hello World

# strings can be concatenated (combined together) using a '+' sign
"Hello" + "World"
#> HelloWorld

# There is no space between the two words. Why? We need to tell Python to print a space
"Hello" + " " + "World"
#> Hello World
```

### Numeric Strings

The `str()` function converts a non-string value to a string.

```python
# But what happens if we concatenate a string and a number?
"2" + 2
#> TypeError: must be str, not int

# Oops! We can't concatenate a string and a Number

## We have to convert the non-string value to a string
"2" + str(2)
#> 22

## Thats the same as
"2" + "2"
#> 22

## What about?
"2+2"
#> 2+2

## Python prints exactly what you tell it to
```

### String to Number Conversion

The conversion function

* `int()` converts a numeric string value to an integer.
* `float()` converts a numeric string value to an float.

```python
# But concatenation is not numeric addition. What if the '+' operator follows a number?
2 + 2
#> 4

# A '+' operator (plus sign) following a number performs addition

# If we have a numeric string value, we can convert it to an integer to do addition
int("2") + 2
#> 4

# Similarly with floats
float("5.2") + 1.5
#> 6.7
```

### Print function

The most basic usage of the [`print()` function](https://docs.python.org/3/library/functions.html#print) has one argument containing a *literal string* enclosed in quotes which will print to a file stream called *standard output*, which is probably your terminal.

Note, in the Python interactive shell, values will be echoed (printed) without using the print function. But in scripts, we will need to use the print function to print to *standard output*, *standard error* or another file stream.

```python
# print a string literal 
print("I am immutable!")
#> I am immutable!

# We can print a number and python will convert it to string
print(2)
#> 2
```

There are several ways to combine strings with other data types using formatting. Here are some examples of different approaches.

## String [Formatting](https://docs.python.org/3/library/string.html#format-string-syntax)

Here are some common ways to combine other values into a string and format it.

```python
# "my num: " + 2
# produces an error:
#     TypeError: can only concatenate str (not "int") to str

# we must convert the int to a str first

## + operator
"my num: " + str(2)
#> my num: 2

# but there are other ways to do this...

# str.format() method
"my num: {}".format(2)
#> my num: 2

# f-string
f"my num: {2}"
#> my num: 2

# printf style
"my num: %d" % (2)
#> my num: 2
```

## References

1. [Python.org: Text Sequence Type — str](https://docs.python.org/3/library/stdtypes.html#textseq)
2. [Corey Schafer - Python Tutorial for Beginners 2: Strings - Working with Textual Data](https://www.youtube.com/watch?v=k9TUPpGqYTo&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU)
