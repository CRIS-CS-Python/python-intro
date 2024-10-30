# ![Chiang Rai International School](../images/logo.png?raw=true) Introduction to Python

## Numbers & Operators

### Integers and Floating Point Numbers

```python
## ints and floats are stored in memory differently
# int (no decimal place)
i = 7
j = 22
# float (or floating point number has decimal place)
f = 7.0

## remember python prints strings literally
print("i + f")
#> i + f

## addition
print(i + j)
#> 29

## combining an int and a float results in a float
print(i + f)
#> 14.0

## subtraction
print(j - i)
#> 15
print(i - j)
#> -15

## multiplication
print(i * j)
#> 154

## exponents
print(i ** 2)  # 7 to the power of 2
#> 49

## division
print(j / i)
#> 3.142857142857143

## floor division (integer division)
print(j // i)
#> 3

## modulo gives the remainder of a division operation
print(j % i)
#> 1

print("{} ÷ {} = {} R {}".format(j, i, (j//i), (j%i)))
#> 22 ÷ 7 = 3 R 1

## printing numbers as strings
# print("i = " + i)
# TypeError: must be str, not int

# convert the int to a string before trying string concatenation
print("i = " + str(i))
#> i = 7

## Different ways of printing numbers

# string concatenations
print("i = " + str(i) + ", j = " + str(j) + ", f = " + str(f))
#> i = 7, j = 22, f = 7.0

# let Python convert for us using the str.format() method
print("i = {}, j = {}, f = {}".format(i, j, f))
#> i = 7, j = 22, f = 7.0

# old school `printf` style using format specifiers
print("i = %s, j = %s, f = %s" % (i, j, f))
#> i = 7, j = 22, f = 7.0

# `printf` with padding and precision. f has a width of 6 with 2 decimal places
print("i = %s, j = %s, f = %6.2f" % (i, j, f))
#> i = 7, j = 22, f =   7.00

# f-string (formatted string literals)
print(f"i = {i}, j = {j}, f = {f:6.2f}")
#> i = 7, j = 22, f =   7.00
```

### Operator Precidence

The video introduces "order of operations".  Here is a pretty good introduction to order of operations and grouping operators:

[Python operator precedence associativity](https://www.techbeamers.com/python-operator-precedence-associativity/)

Here is the authoritative reference:

[Python.org operator precedence](https://docs.python.org/3.3/reference/expressions.html#operator-precedence)

## Additional Study

[Corey Schafer - Integers and Floats](https://www.youtube.com/watch?v=khKv-8q7YmY&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU&index=3)
