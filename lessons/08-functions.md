# ![Chiang Rai International School](../images/logo.png?raw=true) Introduction to Python

## Functions

A function is a reusable blocks of code having a name and *argument list* (also called a parameter list in other languages).

Functions must be *defined* before they can be *called*. The code in a function definition is not executed until it is called.

Every function definition

* starts with a `def` keyword.
* has a name that can be composed of letters, numeric digits, and underscores (`_`).
* has a *formal argument list* of zero or more comma separated variable names between starting and ending parenthesis [`(` and `)`].
* a function *body* indented one level (4 spaces) immediately following the function definition.
* a `return` statement. If not provided in the function deviation, the Python interpreter will return `None` automatically.

Functions are best documented using a `'''docstring comment'''` immediately following the definition.

However, functions once defined, do nothing until they are *called*. The *actual arguments* must be passed into the function in the same position (order) as defined.

### Function Examples

#### Empty parameter list with no `return` statement

Functions can have an empty argument list - nothing between the `(` and `)`  - in the function definition.

```python
def say_hello():
    '''prints a message to standard output'''
    print("hello")

# call function
say_hello()
#> hello
```

The above function is called using `say_hello()`, passing in zero actual arguments. The function body contains a single `print()` statement and does not contain a `return` statement.

#### Argument list with no `return` statement

```python
# function definition
def next_year(age):
    '''accept an age argument and prints next year'''
    age +=1
    print(f"Next year, you will be {age} years old.")

# age here is outside the function, so the `age += 1` statement above does not change it.
age = 14
print(f"You are currently {age} years old.")

# call function
next_year(age)
print(f"You are currently {age} years old.")
```

##### Output

```
You are currently 14 years old.
Next year, you will be 15 years old.
You are currently 14 years old.
```

#### Argument list with `return` statement

Values are returned from a function using the `return` keyword.

```python
# function definition
def add_2(num):
    '''accepts a number argument and returns that value + 2'''
    num +=2
    return num

fav_num = 3
# call the function and use the return value
new_num = add_2(fav_num)
print(f"Favorite number: {fav_num}")
print(f"New number: {new_num}")
```

##### Output

```
Favorite number: 3
New number: 5
```

### Functions Referenced as Objects

A function name can be used as a value like any other value:
assigned to variables, passed into functions, used as values in a dictionary, etc.

#### Function Object Example

```python
def add(num1, num2):
    '''add two given numbers and return the value'''
    return num1 + num2

def subtract(num1, num2):
    '''subtract two given numbers and return the value'''
    return num1 - num2

def multiply(num1, num2):
    '''multiply two given numbers and return the value'''
    return num1 * num2

# call function normally
print("3 + 2 =", add(3, 2))

# function are objects
# print function reference (address in memory)
print(add)

# use a function reference as value for a variable, then call it
calc_func = add
print("5 + 3 =", calc_func(5, 3))

calc_func = multiply
print("5 * 3 =", calc_func(5, 3))
```

##### Output

```
3 + 2 = 5
<function add at 0x7f75c69204a0>
5 + 3 = 8
5 * 3 = 15
```

#### Pure Functions versus Side Effects

A "pure function" is one that is *deterministic* - it predictably returns the
same return value for a given input value. This is how functions work in
mathematics.

The `add()`, `subtract()` and `multiply()` functions above are examples
of pure functions.

However, functions in most computer programming languages are
more general purpose so they don't have to behave like a "pure function" and
can have *side effects*.

A side effect is any thing that changes the state of the system in an
undocumented or unintended way.

For example, writing data to a file inside a function could produce an
unintended side effect of your hard drive filling beyond capacity.

Another example, would be modifying the state of the program such that a global
variable produces non-deterministic results.

This is a great [in-depth discussion](https://hackernoon.com/negating-side-effects-in-python-a-guide-with-pictures)
of side effects and how to remove them.

## References

1. [Corey Schafer - Functions](https://www.youtube.com/watch?v=9Os0o3wzS_I&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU&index=8)