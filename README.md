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

## Python functions
``` python
def my_function(fname):
  print(fname + " Refsnes")

my_function("Emil")
my_function("Tobias")
my_function("Linus")
```
Arbitrary Arguments, \*args: this way the function will receive a tuple of arguments
``` python
def my_function(*kids):
  print("The youngest child is " + kids[2])

my_function("Emil", "Tobias", "Linus")
```
Keyword Arguments:
``` python
def my_function(child3, child2, child1):
  print("The youngest child is " + child3)

my_function(child1 = "Emil", child2 = "Tobias", child3 = "Linus")
```
Arbitrary Keyword Arguments, \*\*kwargs: this way the function will receive a dictionary of arguments
``` python
def my_function(**kid):
  print("His last name is " + kid["lname"])

my_function(fname = "Tobias", lname = "Refsnes")
```
Default parameter value:
``` python
def my_function(country = "Norway"):
  print("I am from " + country)

my_function("Sweden")
my_function("India")
my_function()
my_function("Brazil")
```

## Python recursion
``` python
def tri_recursion(k):
  if(k > 0):
    result = k + tri_recursion(k - 1)
    print(result)
  else:
    result = 0
  return result

print("\n\nRecursion Example Results")
tri_recursion(6)
```

## Python lambda
A lambda function is a small anonymous function. This is functional programming.
``` python
x = lambda a, b, c : a + b + c
print(x(5, 6, 2))
```
``` python
def myfunc(n):
  return lambda a : a * n

mydoubler = myfunc(2)

print(mydoubler(11))
```

## Python modules
``` python
import mymodule

mymodule.greeting("Jonathan")
```
``` python
from mymodule import person1

print (person1["age"])
```

## Python Datetime
Date output:
``` python
import datetime

x = datetime.datetime.now()

print(x.year)
print(x.strftime("%A"))
```
Creating date objects:
``` python
import datetime

x = datetime.datetime(2020, 5, 17)

print(x)
```

## Python Math
``` python
import math

x = math.sqrt(64)

print(x)
```

## Python and JSON
Parse JSON - Convert from JSON to Python:
``` python
import json

# some JSON:
x =  '{ "name":"John", "age":30, "city":"New York"}'

# parse x:
y = json.loads(x)

# the result is a Python dictionary:
print(y["age"])
```
Convert from Python to JSON:
``` python
import json

# a Python object (dict):
x = {
  "name": "John",
  "age": 30,
  "city": "New York"
}

# convert into JSON:
y = json.dumps(x)

# the result is a JSON string:
print(y)
```

## RegEx in Python
``` python
import re

txt = "The rain in Spain"
x = re.search("^The.*Spain$", txt)
```
findall() function - Returns a list containing all matches:
``` python
import re

txt = "The rain in Spain"
x = re.findall("ai", txt)
print(x)
```
search() function - Returns a Match object if there is a match anywhere in the string:
``` python
import re

txt = "The rain in Spain"
x = re.search("\s", txt)

print("The first white-space character is located in position:", x.start())
```
split() function - returns a list where the string has been split at each match:
``` python
import re

txt = "The rain in Spain"
x = re.split("\W", txt)
print(x)
```
sub() function: - replaces the matches with the text of your choice:
``` python
import re

txt = "The rain in Spain"
x = re.sub("\s", "9", txt)
print(x)
```

