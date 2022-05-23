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

## Python Tuples
- Tuple items are ordered, unchangeable, and allow duplicate values.
- To create a tuple with only one item, you have to add a comma after the item, otherwise Python will not recognize it as a tuple.
- Tuple items can be of any data types.

## Python Sets
- Set items are unordered, unchangeable, and do not allow duplicate values.
- Set items can be of any data type.

## Python dictionaries
- Dictionaries are used to store data values in key:value pairs.
- Dictionary items are ordered, changeable, and does not allow duplicates.
- The values in dictionary items can be of any data type.

## Python If ... Else
``` python
a = 200
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
else:
  print("a is greater than b")
```
In short:
``` python
print("A") if a > b else print("=") if a == b else print("B")
```

## Python While loops
``` python
i = 1
while i < 6:
  print(i)
  if i == 3:
    break
  i += 1
```
``` python
i = 0
while i < 6:
  i += 1
  if i == 3:
    continue
  print(i)
```
``` python
i = 1
while i < 6:
  print(i)
  i += 1
else:
  print("i is no longer less than 6")
```

## Python for loops
``` python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  if x == "banana":
    break
  print(x)
```
``` python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  if x == "banana":
    continue
  print(x)
```
``` python
for x in range(6):
  if x == 3: break
  print(x)
else:
  print("Finally finished!")
```
