# ![Chiang Rai International School](images/logo.png?raw=true) Introduction to Python

In this lesson, we will paste the code examples into a file called `strings.py`

And run it from the command line:

## Windows Users

```bash
py strings.py
```

## *NIX Users (Mac, Linux, etc...)

```bash
python3 strings.py
```

## String Indexing & Slicing

In this lesson, we will use *variables* to store values.

A variable is a symbolic name associated with a value stored in memory.

```python
# a variable called `country`, containing the text "thailand"
country = "thailand"

# literally what is between quotes
print("country")
#> country

# prints the contents of the variable
print(country)
#> thailand

# variable names are case sensitive
print(Country)
# > NameError: name 'Country' is not defined

# Concatenation: combining or appending strings
print("Country: " + country)
#> Country: thailand

print("Country: {}".format(country))
#> Country: thailand

city = "chiang rai"

# convert all characters to upper case
print(city.upper())
#> CHIANG RAI

# to lower case
print("THAILAND".lower())
#> thailand

# capitalize only the first character
print(city.capitalize())
#> Chiang rai

# capitialize each word
print(city.title())
#> Chiang Rai

# format the string with a ', ' between values
print("{}, {}".format(city, country).title())
#> Chiang Rai, Thailand
```

## String Indexing

We use the `len()` function to return the length (or number of items) in a sequence, such as a string.

```python
city = "Chiang Mai"

# string length
len(city)
#> 10

# String Indexing
# ---------------
# Strings are a immutable lists of characters
# indexed starting at 0 and ending
# at length - 1.
#
# 0         1
# 012345678901
# Chiang Mai

# Access characters via index
print(city[0])
#> C
print(city[7])
#> M

# The length is 10, but the last index is 9
# print(city[10])
#> IndexError: string index out of range

# Negative Indexes 
# ----------------
# example indexes -10 to -1
#
# 1        
# 0987654321
# Chiang Mai

print(city[-1])
#> i

print(len(city)-1)
#> 9

print(city[9])
#> i

print(city[len(city)-1])
#> i

print(city[-1])
#> i

print(city[-10])
#> C

# the absolute value of negative indexes cannot be
# greater than the absolute value of 0-length
# print(city[-11])
#> IndexError: string index out of range
```

# # String Slicing

We can extract a slice (or substring) from a string.

```python
print(city[0:6])
#> Chiang
print(city[:6])
#> Chiang
print(city[7:len(city)])
#> Mai
print(city[7:10])
#> Mai
print(city[7:])
#> Mai
print(city[-3:10])
#> Mai
print(city[-3:])
#> Mai

# let's change "Chiang Mai" to "Chiang Rai"
print("Chiang Mai"[:7] + "Rai")

String Variables & Indexing
# a variable called *country*, containing the text *thailand*
country = "thailand"

# prints literally what is between quotes
print("country")
#> country

# prints the contents of the variable
print(country)
#> thailand

# variable names are case sensitive
# print(Country)
# > NameError: name 'Country' is not defined

# Concatenation: combining or appending strings
print("Country: " + country)
#> Country: thailand

print("Country: {}".format(country))
#> Country: thailand

city = "chiang rai"

print(city.upper())
#> CHIANG RAI

print("THAILAND".lower())
#> thailand

print(city.capitalize())
#> Chiang rai

print(city.title())
#> Chiang Rai

print("{}, {}".format(city, country).title())
#> Chiang Rai, Thailand

city = "Chiang Mai"

# string length
len(city)
#> 10

# String Indexing
# ---------------
# Strings are a immutable lists of characters
# indexed starting at 0 and ending
# at length - 1.
#
# 0         1
# 012345678901
# Chiang Mai

# Access characters via index
print(city[0])
#> C
print(city[7])
#> M

# The length is 10, but the last index is 9
# print(city[10])
#> IndexError: string index out of range

# Negative Indexes 
# ----------------
# example indexes -10 to -1
#
# 1        
# 0987654321
# Chiang Mai

print(city[-1])
#> i

print(len(city)-1)
#> 9

print(city[9])
#> i

print(city[len(city)-1])
#> i

print(city[-1])
#> i

print(city[-10])
#> C

# the absolute value of negative indexes cannot be
# greater than the absolute value of 0-length
# print(city[-11])
#> IndexError: string index out of range

# String Slicing
print(city[0:6])
#> Chiang
print(city[:6])
#> Chiang
print(city[7:len(city)])
#> Mai
print(city[7:10])
#> Mai
print(city[7:])
#> Mai
print(city[-3:10])
#> Mai
print(city[-3:])
#> Mai

# let's change "Chiang Mai" to "Chiang Rai"
print("Chiang Mai"[:7] + "Rai")