# ![Chiang Rai International School](../images/logo.png?raw=true) Introduction to Python

## Sequences

Sequences are a collection of data in series (one item after another).

### Strings

A string is a sequence of characters.

```python
#       0123456789
name = "John Henry"

# access items given and index integer
print(name[5])   # prints the 'H' in 'John Henry'

# the characters in the string cannot be changed (immutable)
# name[9] = 'i'  # error
```

### Lists

A list is a sequence of values that can be changed (mutable).

```python
#        0  1  2  3  4  5   6
evens = [0, 2, 4, 6, 8, 10, 11]
evens[6] = 12  # change value (mutable)

# access items by integer index
print(evens[5])
#> 10
```

### Tuples

A tuple is a immutable sequence of values.

```python
#         0  1  2  3  4  5    6
primes = (1, 2, 3, 5, 7, 11, 13)
# primes[6] = 12  # error, cannot change values (immutable)

# access items by integer index
print(evens[3])
#> 5
```

### Dictionaries

Dictionaries are a sequence of key/value pairs.

```python
student_heights = {
    'Daniel': 169,
    'Selah': 172,
    'Acer': 175,
    'Kane': 178,
    'Jake': 195
}

# access values with an existing key
print(student_heights['Daniel'])
#> 169

# access non-existing item
# print(student_heights['Sai'])  # key error

# check if key exists
'Sai' in student_heights
#> False

# if item exists, print value, else create item
if 'Sai' in student_heights:
    print(student_heights['Sai'])  # print existing value
else:
    student_heights['Sai'] = 179  # creates new item

'Sai' in student_heights
#> True

# update existing value
student_heights['Kane'] = 179

# dictionary list of keys
print(student_heights.keys())

# dictionary list of values
print(student_heights.values())

# dictionary items as a list of tuples: [(key, value) ...]
print(student_heights.items())

# iterate over keys
print("Iterate Keys")
for key in student_heights:
    # print key:value
    print("{}:{}".format(key, student_heights[key]))

# iterate over items, unpacking each tuple
print("Iterate Items")
for key, val in student_heights.items():
    # print key:value
    print("{}:{}".format(key, val))
```

### `list.sort()`

The `list.sort()` method sorts a list in place, meaning the list is changed

```python
counting_nums = [3, 1, 9, 2, 5, 8, 4, 10, 7, 6]
counting_nums.sort()
print(counting_nums)
#> [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# reverse order
counting_nums.sort(reverse=True)
print(counting_nums)
#> [10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
```

### `sorted()`

Returns a sorted copy of a list. The original list is not changed.
It also has a `reverse` option.

```python
messy_nums = [3, 1, 9, 2, 5, 8, 4, 10, 7, 6]
counting_nums = sorted(messy_nums)
print(counting_nums)
#> [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
print(messy_nums)  # messy_nums not changed
#> [3, 1, 9, 2, 5, 8, 4, 10, 7, 6]
```

### Sort Dictionary by Key

```python
# list of dictionary items sorted by value descending (greatest values first)
sorted_by_val = sorted(student_heights.items(), key=lambda item: item[1], reverse=True)

# print student height from tallest to shortest
print("Student Heights Sorted in Reverse:")
for key, val in sorted_by_val:
    print("{}:{}".format(key, val))
```

## References

1. [Python.org: Data Structures](https://docs.python.org/3/tutorial/datastructures.html)
1. [Corey Schafer - Lists, Tuples, Sets](https://www.youtube.com/watch?v=daefaLgNkw0&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU&index=4)
1. [Corey Schafer - Dictionaries](https://www.youtube.com/watch?v=daefaLgNkw0&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU&index=5)
1. [Google Students AC101 - Lists](https://www.youtube.com/watch?v=mrwSbE5MDn0)
1. [Google Students AC101 - Loops](https://www.youtube.com/watch?v=X1-UNHUajfk)
1. [Google Students AC101 - Mutability](https://www.youtube.com/watch?v=fnSijYDKz3c)
1. [Google Students AC101 - Key Value Pairs](https://www.youtube.com/watch?v=eDQ19ahXsSk)
