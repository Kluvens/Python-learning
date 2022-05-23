# Python-learning

## Python comments
```#``` for one line commenting and ```""" """``` for multiple lines of commenting

## Global variables
we should reference the global variable before modifying it
``` python
x = "awesome"

def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x)
```

## Data types
types include: ```str, int, float, complex(for complex numbers), list, tuple, dict, set, bool, None```

## Python casting
use ```int(), str(), float() etc.``` to specify a type on to a variable.

## Python strings
In python, ```'hello'``` is the same as ```"hello"```

Multiline String:
``` python
a = """Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua."""
print(a)
```

Slicing string:
``` python
b = "Hello, World!"
print(b[2:5])
```

Modify strings:
we can use built-in methods to modify strings:
- ```.uppper()``` - string to upper case
- ```.strip()``` -  removes any whitespace from the beginning or the end
- ```.replace()``` - replaces a string with another string
- ```.split()``` - splits the string into substrings if it finds instances of the separator

## Python operators

### Arithmetic operators
- ```+``` - addition
- ```-``` - subtraction
- ```*``` - multiplication
- ```/``` - division
- ```%``` - modulus
- ```**``` - exponentiation
- ```//``` - floor division

### Assignment operators
```
=, +=, -=, *=, /=, %=, //=, **=, &=, |=, ^=, >>=, <<=
```

### Comparison operators
```
==, !=, <, >, <=, >=
```

### Logical operators
```
and, or, not
```

### Identity operators
```
is, is not
```

### Membership operators
```
in, not in
```

### Bitwise operators
```
&, |, ^, ~, >>, <<
```

## Python Lists
- List items are ordered, changeable, and allow duplicate values.
- List items can be of any data type.


