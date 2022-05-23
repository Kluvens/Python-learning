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
