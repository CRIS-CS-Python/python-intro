# ![Chiang Rai International School](../images/logo.png?raw=true) Introduction to Python

Input & Output (I/O) is how a *process* (a running program) receives or sends data to devices.
In this lesson, we will input and output character data from and to the terminal.

## Standard I/O

There are three file streams available to a process started in a terminal:

* *standard output (STDOUT)* - default output file stream
* *standard input (STDIN)* - default input file stream
* *standard error (STDERR)* - default output file stream for errors

```
                +-----------+
    STDIN --->  |  Process  | ---> STDOUT 
                +-----------+
                      |
                      +---> STDERR
```

## Standard Output (STDOUT)

The `print()` function is the most common way to output text data (strings).

```python
# writes string to the STDOUT file stream
print("Hello World")
```

## Standard Input (STDIN)

The `input(prompt)`
* Prints a prompt to STDOUT without a trailine newline character.
* Waits for the user to type input data and press `<enter>`.
* Pressing `<enter>` sends a *newline character* (`\n`) which causes the function to return the value entered as a **string**.

```python
# writes "What is your name? " to STDOUT
# and returns the text entered as a string
name = input("What is your name? ")

# name contains the string entered (but not the newline)
```

### Inputting Numbers

Since `input()` returns a string, you will need to convert numbers using
the appropriate conversion function, such as `int()` or `float()`

```python
age_str = input("How old are you? ")
# age_str + 1 will fail because it tries to do string concatenation
age = int(age_str)
# age + 1 is okay becase age is an int
print("Next year, you will be {} years old.".format(age + 1))
```

## Input from Command Line

We can pass text data into a process when we start it using *command line arguments*.
`sys.argv` is a list of string arguments to the process. The first argument is always
the command that executed the process.

Save this to a file `cmd_args.py`

```python
import sys
# prints a list of string arguments
print(sys.argv)
```

Runtime example:

```bash
$ py cmd_args.py
['cmd_args.py']
$ py cmd_args.py 1 two III
['cmd_args.py', '1', 'two', 'III']
```

## Standard Error (STDERR)

`sys.stderr` is a *file object* than when written to, will send
STDERR data to the terminal. The terminal can separate STDOUT and STDERR
if needed.

```python
import sys
# writes string to the STDERR file stream
print("This should not happen!", file=sys.stderr)
```

## References

1. [Python.org: Input and Output](https://docs.python.org/3/tutorial/inputoutput.html)
