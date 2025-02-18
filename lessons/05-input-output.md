# ![Chiang Rai International School](../images/logo.png?raw=true) Introduction to Python

Input & Output (I/O) is how a *process* (a running program) receives or sends data to devices.
In this lesson, we will input and output character data from and to the terminal.

## Standard I/O

There are three file streams available to a process started in a terminal:

* *standard input (STDIN)* - default input file stream having file descriptor 0
* *standard output (STDOUT)* - default output file stream having file descriptor 1
* *standard error (STDERR)* - default output file stream for errors having file descriptor 2

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

* Prints a prompt to STDOUT followed by a newline character.
* Waits for the user to type input data and press `<enter>`.
* Pressing `<enter>` sends a *newline character* (`\n`) which causes
  the function to return the value entered as a **string**.

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
`sys.argv` is a list of string arguments for the process. The first argument is always
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
STDERR data to the terminal. The terminal can
[separate STDOUT and STDERR](https://tldp.org/HOWTO/Bash-Prog-Intro-HOWTO-3.html)
if needed.

```python
import sys
# writes string to the STDERR file stream
print("This should not happen!", file=sys.stderr)
```

### Open and Read Text Files

This example opens a file, but lets Python close the file for us using a
`with` context block. Next, we iterate over the file object one line at a time.
`line` is a string containing the text for that line it the file.

```python
# open file and print each line one at a time
with open("myfile.txt") as fh:
  for line in fh:
    print(line, end='') # line already contains the '\n' at the end
```

## References

1. [Python.org: Input and Output](https://docs.python.org/3/tutorial/inputoutput.html)
1. [Google Students AC101 - Files](https://www.youtube.com/watch?v=zASE-UA2YKg)
