# Quick-Referenz Python

## Importieren

```python
# 'generic import' of math module
import math
math.sqrt(25)

# import a function
from math import sqrt
sqrt(25)  # no longer have to reference the module

# import multiple functions at once
from math import cos, floor

# import all functions in a module (generally discouraged)
from csv import *

# define an alias
import datetime as dt

# show all functions in math module
x=dir(math)

# System
import sys 
sys.exit()
```

## Datentypen

```python
# determine the type of an object
type(2)        # returns 'int'
type(2.0)      # returns 'float'
type('two')    # returns 'str'
type(True)     # returns 'bool'
type(None)     # returns 'NoneType'

# check if an object is of a given type
isinstance(2.0, int)  # returns False
isinstance(2.0, (int, float))  # returns True

# convert an object to a given type
float(2)
int(2.9)
str(2.9)

# zero, None, and empty containers are converted to False
bool(0)
bool(None)
bool('')  # empty string
bool([])  # empty list
bool({})  # empty dictionary

# non-empty containers and non-zeros are converted to True
bool(2)
bool('two')
bool([2])
```

## Operatoren

```python
# basic operations
10 + 4         # add (returns 14)
10 - 4         # subtract (returns 6)
10 * 4         # multiply (returns 40)
10 **4         # exponent (returns 10000)
5  % 4         # modulo (returns 1) - computes the remainder
10 / 4         # divide (returns 2 in Python 2, returns 2.5 in Python 3)
10 / float(4)  # divide (returns 2.5)

# force '/' in Python 2 to perform 'true division' (unnecessary in Python 3)
# from __future__ import division

10 /  4        # true division (returns 2.5)
10 // 4        # floor division (returns 2)
```

## Vergleichs- und Boolean-Operationen

```python
# assignment statement
x = 5

# comparisons (these return True)
x >  3
x >= 3
x != 3
x == 5

# boolean operations (these return True)
5 > 3 and 6 > 3
5 > 3 or 5 < 3
not False
False or not False and True  # evaluation order: not, and, or
```

## Bedingungen

```python
# if statement
x = 1
if x > 0:
    print('positive')

# if/else statement
if x > 0:
    print('positive')
else:
    print('zero or negative')

# if/elif/else statement
if x > 0:
    print('positive')
elif x == 0:
    print('zero')
else:
    print('negative')

# single-line if statement (sometimes discouraged)
if x > 0: print('positive')

# single-line if/else statement (sometimes discouraged)
# known as a 'ternary operator'
msg = 'positive' if x > 0 else 'zero or negative'
# The first statement (True or “Some”) will return True 
# and the second statement (False or “Some”) will return Some.

output = None
msg    = output or "No data returned"
print(msg)
# No data returned
```

## Listen

```python
# properties: ordered, iterable, mutable, can contain multiple data types

# create an empty list (two ways)
empty_list = []
empty_list = list()

# create a list
simpsons = ['homer', 'marge', 'bart']

# examine a list
simpsons[0]    # print element 0 ('homer')
len(simpsons)  # returns the length (3)

# modify a list (does not return the list)
simpsons.append('lisa')                 # append element to end
simpsons.extend(['itchy', 'scratchy'])  # append multiple elements to end
simpsons.insert(0, 'maggie')            # insert element at index 0
                                        # and shifts everything right
simpsons.remove('bart')                 # search for first instance 
                                        # and remove it
simpsons.pop(0)                         # remove element 0 and return it
del simpsons[0]                         # remove element 0 and
                                        # does not return it
simpsons[0] = 'krusty'                  # replace element 0

# concatenate lists (slower than 'extend' method)
neighbors = simpsons + ['ned', 'rod', 'todd']

# find elements in a list
simpsons.count('lisa')     # counts the number of instances
simpsons.index('itchy')    # returns index of first instance

# list slicing [start:end:step]
weekdays = ['mon', 'tues', 'wed', 'thurs', 'fri']
weekdays[0]    # element 0
weekdays[0:3]  # elements 0, 1, 2
weekdays[:3]   # elements 0, 1, 2
weekdays[3:]   # elements 3, 4
weekdays[-1]   # last element (element 4)
weekdays[::2]  # every 2nd element (0, 2, 4)
weekdays[::-1] # backwards (4, 3, 2, 1, 0)

# alternative method for returning the list backwards
list(reversed(weekdays))

# sort a list in place (modifies but does not return the list)
simpsons.sort()
simpsons.sort(reverse=True)  # sort in reverse
simpsons.sort(key=len)       # sort by a key

# return a sorted list (does not modify the original list)
sorted(simpsons)
sorted(simpsons, reverse=True)
sorted(simpsons, key=len)

# insert into an already sorted list, and keep it sorted
num = [10, 20, 40, 50]
from bisect import insort
insort(num, 30)

# create a second reference to the same list
same_num    = num
same_num[0] = 0  # modifies both 'num' and 'same_num'

# copy a list (two ways)
new_num = num[:]
new_num = list(num)

# examine objects
num is same_num  # returns True (checks whether they are the same object)
num is new_num   # returns False
num == same_num  # returns True (checks whether they have the same contents)
num == new_num   # returns True
```

## Tuples (wie Listen, nur unveränderlich in Typ und Größe)

```python
## properties: ordered, iterable, immutable, can contain multiple data types
## like lists, but they don't change size

# create a tuple
digits = (0, 1, 'two')         # create a tuple directly
digits = tuple([0, 1, 'two'])  # create a tuple from a list
zero = (0, )                   # trailing comma is required 
                               # to indicate it's a tuple

# examine a tuple
digits[2]        # returns 'two'
len(digits)      # returns 3
digits.count(0)  # counts the number of instances of that value (1)
digits.index(1)  # returns the index of the first instance of that value (1)

# elements of a tuple cannot be modified
# digits[2] = 2 # throws an error

# concatenate tuples
digits = digits + (3, 4)

# create a single tuple with elements repeated (also works with lists)
(3, 4) * 2    # returns (3, 4, 3, 4)

# sort a list of tuples
tens = [(20, 60), (10, 40), (20, 30)]
sorted(tens)  # sorts by first element in tuple, then second element
              # returns [(10, 40), (20, 30), (20, 60)]

# tuple unpacking
bart = ('male', 10, 'simpson')  # create a tuple
(sex, age, surname) = bart      # assign three values at once
```

## Strings

```python
## properties: iterable, immutable

# create a string
s = str(42)        # convert another data type into a string
s = 'I like you'

# examine a string
s[0]               # returns 'I'
len(s)             # returns 10
 
# string slicing is like list slicing
s[:6]              # returns 'I like'
s[7:]              # returns 'you'
s[-1]              # returns 'u'

# basic string methods (does not modify the original string)
s.lower()                  # returns 'i like you'
s.upper()                  # returns 'I LIKE YOU'
s.startswith('I')          # returns True							
s.endswith('you')          # returns True
s.isdigit()                # returns False (returns True if every character 
                           # in the string is a digit)
s.find('like')             # returns index of first occurrence (2), 
                           # but doesn't support regex
s.find('hate')             # returns -1 since not found
s.replace('like', 'love')  # replaces all instances of 'like' with 'love'

# split a string into a list of substrings separated by a delimiter
s.split(' ')               # returns ['I', 'like', 'you']
s.split()                  # equivalent (since space is the default 
                           # delimiter)
s2 = 'a, an, the'
s2.split(',')              # returns ['a', ' an', ' the']

# join a list of strings into one string using a delimiter
stooges = ['larry', 'curly', 'moe']
' '.join(stooges)          # returns 'larry curly moe'

# concatenate strings
s3 = 'The meaning of life is'
s4 = '42'
s3 + ' ' + s4              # returns 'The meaning of life is 42'

# remove whitespace from start and end of a string
s5 = '  ham and cheese  '
s5.strip()                 # returns 'ham and cheese'

# string substitutions: all of these return 'raining cats and dogs'
'raining %s and %s' % ('cats', 'dogs')                        # old way
'raining {} and {}'.format('cats', 'dogs')                    # new way
'raining {arg1} and {arg2}'.format(arg1='cats', arg2='dogs')  # named arguments

# string formatting
# more examples: https://mkaz.blog/code/python-string-format-cookbook/
'pi is {:.2f}'.format(3.14159)    # returns 'pi is 3.14'

# normal strings versus raw strings
print('first line\nsecond line')  # normal strings allow 
                                  # for escaped characters
print(r'first line\nfirst line')  # raw strings treat 
                                  # backslashes as literal characters
```

## Dictionaries (Listen von Schlüssel-Werte-Paaren also Key/Value)

```python
## properties: unordered, iterable, mutable, can contain multiple data types
## made of key-value pairs
## keys must be unique, and can be strings, numbers, or tuples
## values can be any type

# create an empty dictionary (two ways)
empty_dict = {}
empty_dict = dict()

# create a dictionary (two ways)
family = {'dad': 'homer', 'mom': 'marge', 'size': 6}
family = dict(dad='homer', mom='marge', size=6)

# convert a list of tuples into a dictionary
list_of_tuples = [('dad', 'homer'), ('mom', 'marge'), ('size', 6)]
family = dict(list_of_tuples)

# examine a dictionary
family['dad']      # returns 'homer'
len(family)        # returns 3
'mom' in family    # returns True
'marge' in family  # returns False (only checks keys)

# returns a list (Python 2) or an iterable view (Python 3)
family.keys()      # keys: ['dad', 'mom', 'size']
family.values()    # values: ['homer', 'marge', 6]
family.items()     # key-value pairs: [('dad', 'homer'), ('mom', 'marge'), ('size', 6)]

# modify a dictionary (does not return the dictionary)
family['cat'] = 'snowball'                           # add a new entry
family['cat'] = 'snowball ii'                        # edit an existing entry
del family['cat']                                    # delete an entry
family['kids'] = ['bart', 'lisa']                    # dictionary value can be a list
family.pop('dad')                                    # remove an entry and 
                                                     # return the value ('homer')
family.update({'baby': 'maggie', 'grandpa': 'abe'})  # add multiple entries

# access values more safely with 'get'
family['mom']                       # returns 'marge'
family.get('mom')                   # equivalent
#family['grandma']                  # throws an error since the key does not exist
family.get('grandma')               # returns None instead
family.get('grandma', 'not found')  # returns 'not found' (the default)

# access a list element within a dictionary
family['kids'][0]              # returns 'bart'
family['kids'].remove('lisa')  # removes 'lisa'

# string substitution using a dictionary
'youngest child is %(baby)s' % family  # returns 'youngest child is maggie'
```

## Sets (wie Dictionaries, aber nur Schlüssel, keine Werte)

```python
## properties: unordered, iterable, mutable, can contain multiple data types
## made of unique elements (strings, numbers, or tuples)
## like dictionaries, but with keys only (no values)

# create an empty set
empty_set = set()

# create a set
languages = {'python', 'r', 'java'}         # create a set directly
snakes = set(['cobra', 'viper', 'python'])  # create a set from a list

# examine a set
len(languages)         # returns 3
'python' in languages  # returns True

# set operations
languages & snakes  # returns intersection: {'python'}
languages | snakes  # returns union: {'cobra', 'r', 'java', 'viper', 'python'}
languages - snakes  # returns set difference: {'r', 'java'}
snakes - languages  # returns set difference: {'cobra', 'viper'}

# modify a set (does not return the set)
languages.add('sql')              # add a new element
languages.add('r')                # try to add an existing element (ignored, no error)
languages.remove('java')          # remove an element
#languages.remove('c')            # try to remove a non-existing element (throws an error)
languages.discard('c')            # remove an element if present, but ignored otherwise
languages.pop()                   # remove and return an arbitrary element
languages.clear()                 # remove all elements
languages.update(['go','spark'])  # add multiple elements (can also pass a set)

# get a sorted list of unique elements from a list
sorted(set([9, 0, 2, 1, 0]))      # returns [0, 1, 2, 9]
```

## Funktionen definieren

```python
# define a function with no arguments and no return values

def print_text():
    print('this is text')


# call the function
print_text()


# define a function with one argument and no return values
def print_this(x):
    print(x)


# call the function
print_this(3)      # prints 3
n = print_this(3)  # prints 3, but doesn't assign 3 to n

#   because the function has no return statement


# define a function with one argument and one return value
def square_this(x):
    return x**2


# include an optional docstring to describe the effect of a function
def square_this(x):
    """Return the square of a number."""
    return x**2


# call the function
square_this(3)        # prints 9
var = square_this(3)  # assigns 9 to var, but does not print 9


# define a function with two 'positional arguments' (no default values) and
# one 'keyword argument' (has a default value)
def calc(a, b, op='add'):
    if op == 'add':
        return a + b
    elif op == 'sub':
        return a - b
    else:
        print('valid operations are add and sub')


# call the function
calc(10, 4, op='add')  # returns 14
calc(10, 4,'add')      # also returns 14: unnamed arguments are inferred by position
calc(10, 4)            # also returns 14: default for 'op' is 'add'
calc(10, 4, 'sub')     # returns 6
calc(10, 4, 'div')     # prints 'valid operations are add and sub'


# use 'pass' as a placeholder if you haven't written the function body
def stub():
    pass


# return two values from a single function
def min_max(nums):
    return min(nums), max(nums)


# return values can be assigned to a single variable as a tuple
nums = [1, 2, 3]
min_max_num = min_max(nums)       # min_max_num = (1, 3)

# return values can be assigned into multiple variables using tuple unpacking
min_num, max_num = min_max(nums)  # min_num = 1, max_num = 3
```

## Anonyme (Lambda) Funktionen

```python
## primarily used to temporarily define a function for use by another function

# define a function the "usual" way
def squared(x):
    return x**2

# define an identical function using lambda
squared = lambda x: x**2

# sort a list of strings by the last letter (without using lambda)
simpsons = ['homer', 'marge', 'bart']

def last_letter(word):
    return word[-1]
sorted(simpsons, key=last_letter)

# sort a list of strings by the last letter (using lambda)
sorted(simpsons, key=lambda word: word[-1])
```

## For- und While-Schleifen

```python

# range returns a list of integers (Python 2) or a sequence (Python 3)
range(0, 3)     # returns [0, 1, 2]: includes start value but excludes stop value
range(3)        # equivalent: default start value is 0
range(0, 5, 2)  # returns [0, 2, 4]: third argument is the step value

# Python 2 only: use xrange to create a sequence rather than a list (saves memory)
# xrange(100, 100000, 5)

# for loop (not the recommended style)
fruits = ['apple', 'banana', 'cherry']
for i in range(len(fruits)):
    print(fruits[i].upper())

# for loop (recommended style)
for fruit in fruits:
    print(fruit.upper())

# iterate through two things at once (using tuple unpacking)
family = {'dad': 'homer', 'mom': 'marge', 'size': 6}
for key, value in family.items():
    print(key, value)

# use enumerate if you need to access the index value within the loop
for index, fruit in enumerate(fruits):
    print(index, fruit)

# for/else loop
for fruit in fruits:
    if fruit == 'banana':
        print('Found the banana!')
        break  # exit the loop and skip the 'else' block
else:
    # this block executes ONLY if the for loop completes without hitting 'break'
    print("Can't find the banana")

# while loop
count = 0
while count < 5:
    print('This will print 5 times')
    count += 1 # equivalent to 'count = count + 1
```

## Comprehensions

```python
# for loop to create a list of cubes
nums  = [1, 2, 3, 4, 5]
cubes = []
for num in nums:
    cubes.append(num**3)

# equivalent list comprehension
cubes = [num**3 for num in nums]     # [1, 8, 27, 64, 125]

# for loop to create a list of cubes of even numbers
cubes_of_even = []
for num in nums:
    if num % 2 == 0:
        cubes_of_even.append(num**3)

# equivalent list comprehension
# syntax: [expression for variable in iterable if condition]
cubes_of_even = [num**3 for num in nums if num % 2 == 0]       # [8, 64]

# for loop to cube even numbers and square odd numbers
cubes_and_squares = []
for num in nums:
    if num % 2 == 0:
        cubes_and_squares.append(num**3)
    else:
        cubes_and_squares.append(num**2)

# equivalent list comprehension (using a ternary expression)
# syntax: [true_condition if condition else false_condition for variable in iterable]
cubes_and_squares = [num**3 if num % 2 == 0 else num**2 for num in nums]  # [1, 8, 9, 64, 25]

# for loop to flatten a 2d-matrix
matrix = [[1, 2], [3, 4]]
items = []
for row in matrix:
    for item in row:
        items.append(item)

# equivalent list comprehension
items = [item for row in matrix for item in row]   # [1, 2, 3, 4]

# set comprehension
fruits = ['apple', 'banana', 'cherry']
unique_lengths = {len(fruit) for fruit in fruits}  # {5, 6}

# dictionary comprehension
fruit_lengths = {fruit: len(fruit) for fruit in fruits}
    # {'apple': 5, 'banana': 6, 'cherry': 6}
fruit_indices = {fruit: index for index, fruit in enumerate(fruits)}
    # {'apple': 0, 'banana': 1, 'cherry': 2}
```

## Maps und Filter

```python
# 'map' applies a function to every element of a sequence
# ...and returns a list (Python 2) or iterator (Python 3)

simpsons = ['homer', 'marge', 'bart']
map(len, simpsons)                    # returns [5, 5, 4]
map(lambda word: word[-1], simpsons)  # returns ['r', 'e', 't']

# equivalent list comprehensions
[len(word) for word in simpsons]
[word[-1] for word in simpsons]

# 'filter' returns a list (Python 2) or iterator (Python 3) containing
# ...the elements from a sequence for which a condition is True
nums = range(5)
filter(lambda x: x % 2 == 0, nums)  # returns [0, 2, 4]

# equivalent list comprehension
[num for num in nums if num % 2 == 0]
```

## Ausnahmebehandlung (Fehler- Try/Except-Block)

```python
try:
  print("Hello")
except:
  print("Something went wrong")
else:
  print("Nothing went wrong")
finally:
  print("The 'try except' is finished")


try:
    except ZeroDivisionError as err:
        print('Handling run-time error:', err)


raise NameError('HiThere')
```

## Python Built-in Exceptions:

```
AssertionError        Raised when assert statement fails.  
AttributeError        Raised when attribute assignment or reference fails.
EOFError              Raised when the input() functions hits end-of-file condition.
FloatingPointError    Raised when a floating point operation fails.
GeneratorExit         Raise  when a generator's close() method is called.
ImportError           Raised when the imported module is not found.
IndexError            Raised when index of a sequence is out of range.
KeyError              Raised when a key is not found in a dictionary.
KeyboardInterrupt     Raised when the user hits interrupt key (Ctrl+c or delete).
MemoryError           Raised when an operation runs out of memory.
NameError             Raised when a variable is not found in local or global scope.
NotImplementedError   Raised by abstract methods.
OSError               Raised when system operation causes system related error.
OverflowError         Raised when result of an arithmetic operation is too large to be represented.
ReferenceError        Raised when a weak reference proxy is used to access a garbage collected referent.
RuntimeError          Raised when an error does not fall under any other category.
StopIteration         Raised by next() function to indicate that there is no further item 
                             to be returned by iterator.
SyntaxError           Raised by parser when syntax error is encountered.
IndentationError      Raised when there is incorrect indentation.
TabError              Raised when indentation consists of inconsistent tabs and spaces.
SystemError           Raised when interpreter detects internal error.
SystemExit            Raised by sys.exit() function.
TypeError             Raised when a function or operation is applied to an object of incorrect type.
UnboundLocalError     Raised when a reference is made to a local variable in a 
                             function or method, but no value has been bound to that variable.
UnicodeError          Raised when a Unicode-related encoding or decoding error occurs.
UnicodeEncodeError    Raised when a Unicode-related error occurs during encoding.
UnicodeDecodeError    Raised when a Unicode-related error occurs during decoding.
UnicodeTranslateError Raised when a Unicode-related error occurs during translating.
ValueError            Raised when a function gets argument of correct type but improper value.
ZeroDivisionError     Raised when second operand of division or modulo operation is zero.
```

## Eingebaute Funktionen

The Python interpreter has a number of functions and types built into it that are always available. They are listed here in alphabetical order.

|               |             |              |              |                     |
| ------------- | ----------- | ------------ | ------------ | ------------------- |
| abs()         | delattr()   | hash()       | memoryview() | set()               |
| all()         | dict()      | help()       | min()        | setattr()           |
| any()         | dir()       | hex()        | next()       | slice()             |
| ascii()       | divmod()    | id()         | object()     | sorted()            |
| bin()         | enumerate() | input()      | oct()        | staticmethod()      |
| bool()        | eval()      | int()        | open()       | str()               |
| breakpoint()  | exec()      | isinstance() | ord()        | sum()               |
| bytearray()   | filter()    | issubclass() | pow()        | super()             |
| bytes()       | float()     | iter()       | print()      | tuple()             |
| callable()    | format()    | len()        | property()   | type()              |
| chr()         | frozenset() | list()       | range()      | vars()              |
| classmethod() | getattr()   | locals()     | repr()       | zip()               |
| compile()     | globals()   | map()        | reversed()   | \_\_ import \_\_ () |
| complex()     | hasattr()   | max()        | round()      | abs(x)              |

## \_

* [ ] future Future statement definitions
* [ ] main The environment where the top-level script is run.
* [ ] dummy\_thread Drop-in replacement for the \_thread module.
* [ ] thread Low-level threading API.

​

## a

* [ ] abc Abstract base classes according to :pep:`3119`.
* [ ] aifc Read and write audio files in AIFF or AIFC format.
* [ ] **argparse** Command-line option and argument parsing library.
* [ ] **array** Space efficient arrays of uniformly typed numeric values.
* [ ] ast Abstract Syntax Tree classes and manipulation.
* [ ] asynchat Support for asynchronous command/response protocols.
* [ ] asyncio Asynchronous I/O.
* [ ] asyncore A base class for developing asynchronous socket handling services.
* [ ] atexit Register and execute cleanup functions.
* [ ] audioop Manipulate raw audio data.

## b

* [ ] base64 RFC 3548: Base16, Base32, Base64 Data Encodings; Base85 and Ascii85
* [ ] **bdb** Debugger framework.
* [ ] **binascii** Tools for converting between binary and various ASCII-encoded binary representations.
* [ ] **binhex** Encode and decode files in binhex4 format.
* [ ] **bisect** Array bisection algorithms for binary searching.
* [ ] builtins The module that provides the built-in namespace.
* [ ] bz2 Interfaces for bzip2 compression and decompression.

## c

* [ ] **calendar** Functions for working with calendars, including some emulation of the Unix cal program.
* [ ] cgi Helpers for running Python scripts via the Common Gateway Interface.
* [ ] cgitb Configurable traceback handler for CGI scripts.
* [ ] chunk Module to read IFF chunks.
* [ ] cmath Mathematical functions for complex numbers.
* [ ] **cmd** Build line-oriented command interpreters.
* [ ] **code** Facilities to implement read-eval-print loops.
* [ ] codecs Encode and decode data and streams.
* [ ] codeop Compile (possibly incomplete) Python code.
* [ ] \- collections Container datatypes
* [ ] colorsys Conversion functions between RGB and other color systems.
* [ ] compileall Tools for byte-compiling all Python source files in a directory tree.
* [ ] \- concurrent
* [ ] configparser Configuration file parser.
* [ ] contextlib Utilities for with-statement contexts.
* [ ] contextvars Context Variables
* [ ] **copy** Shallow and deep copy operations.
* [ ] copyreg Register pickle support functions.
* [ ] cProfile
* [ ] crypt (Unix) The crypt() function used to check Unix passwords.
* [ ] csv Write and read tabular data to and from delimited files.
* [ ] **ctypes** A foreign function library for Python.
* [ ] \*_curses_- \[ ] (Unix) An interface to the curses library, providing portable terminal handling.

## d

* [ ] dataclasses Generate special methods on user-defined classes.
* [ ] **datetime** Basic date and time types.
* [ ] \- dbm Interfaces to various Unix "database" formats.
* [ ] decimal Implementation of the General Decimal Arithmetic Specification.
* [ ] **difflib** Helpers for computing differences between objects.
* [ ] **dis** Disassembler for Python bytecode.
* [ ] \- **distutils** Support for building and installing Python modules into an existing Python installation.
* [ ] **doctest** Test pieces of code within docstrings.
* [ ] **dummy\_threading** Drop-in replacement for the threading module.

## e

* [ ] \- **email** Package supporting the parsing, manipulating, and generating email messages.
* [ ] \- encodings
* [ ] ensurepip Bootstrapping the "pip" installer into an existing Python installation or virtual environment.
* [ ] **enum** Implementation of an enumeration class.
* [ ] **errno** Standard errno system symbols.

## f

* [ ] faulthandler Dump the Python traceback.
* [ ] fcntl (Unix) The fcntl() and ioctl() system calls.
* [ ] **filecmp** Compare files efficiently.
* [ ] **fileinput** Loop over standard input or a list of files.
* [ ] fnmatch Unix shell style filename pattern matching.
* [ ] **formatter** **Deprecated**: Generic output formatter and device interface.
* [ ] **fractions** Rational numbers.
* [ ] ftplib FTP protocol client (requires sockets).
* [ ] **functools** Higher-order functions and operations on callable objects.

## g

* [ ] **gc** Interface to the cycle-detecting garbage collector.
* [ ] **getopt** Portable parser for command line options; support both short and long option names.
* [ ] getpass Portable reading of passwords and retrieval of the userid.
* [ ] gettext Multilingual internationalization services.
* [ ] glob Unix shell style pathname pattern expansion.
* [ ] grp (Unix) The group database (getgrnam() and friends).
* [ ] **gzip** Interfaces for gzip compression and decompression using file objects.

## h

* [ ] **hashlib** Secure hash and message digest algorithms.
* [ ] heapq Heap queue algorithm (a.k.a. priority queue).
* [ ] hmac Keyed-Hashing for Message Authentication (HMAC) implementation
* [ ] \- **html** Helpers for manipulating HTML.
* [ ] \- http HTTP status codes and messages

## i

* [ ] imaplib IMAP4 protocol client (requires sockets).
* [ ] imghdr Determine the type of image contained in a file or byte stream.
* [ ] imp Deprecated: Access the implementation of the import statement.
* [ ] \- importlib The implementation of the import machinery.
* [ ] **inspect** Extract information and source code from live objects.
* [ ] **io** Core tools for working with streams.
* [ ] ipaddress IPv4/IPv6 manipulation library.
* [ ] **itertools** Functions creating iterators for efficient looping.

## j

* [ ] \- json Encode and decode the JSON format.

## k

* [ ] keyword Test whether a string is a keyword in Python.

## l

* [ ] lib2to3 The 2to3 library
* [ ] linecache Provides random access to individual lines from text files.
* [ ] locale Internationalization services.
* [ ] \- **logging** Flexible event logging system for applications.
* [ ] lzma A Python wrapper for the liblzma compression library.

## m

* [ ] mailbox Manipulate mailboxes in various formats
* [ ] mailcap Mailcap file handling.
* [ ] **marshal** Convert Python objects to streams of bytes and back (with different constraints).
* [ ] **math** Mathematical functions (sin() etc.).
* [ ] mimetypes Mapping of filename extensions to MIME types.
* [ ] mmap Interface to memory-mapped files for Unix and Windows.
* [ ] modulefinder Find modules used by a script.
* [ ] msilib (Windows) Creation of Microsoft Installer files, and CAB files.
* [ ] msvcrt (Windows) Miscellaneous useful routines from the MS VC++ runtime.
* [ ] \- **multiprocessing** Process-based parallelism.

## n

* [ ] netrc Loading of .netrc files.
* [ ] nis (Unix) Interface to Sun's NIS (Yellow Pages) library.
* [ ] nntplib NNTP protocol client (requires sockets).
* [ ] numbers Numeric abstract base classes (Complex, Real, Integral, etc.).

## o

* [ ] **operator** Functions corresponding to the standard operators.
* [ ] optparse Deprecated: Command-line option parsing library.
* [ ] \- **os** Miscellaneous operating system interfaces.
* [ ] ossaudiodev (Linux, FreeBSD) Access to OSS-compatible audio devices.

## p

* [ ] parser Access parse trees for Python source code.
* [ ] pathlib Object-oriented filesystem paths
* [ ] **pdb** The Python debugger for interactive interpreters.
* [ ] pickle Convert Python objects to streams of bytes and back.
* [ ] pickletools Contains extensive comments about the pickle protocols and pickle-machine opcodes, as well as some useful functions.
* [ ] pipes (Unix) A Python interface to Unix shell pipelines.
* [ ] pkgutil Utilities for the import system.
* [ ] platform Retrieves as much platform identifying data as possible.
* [ ] plistlib Generate and parse Mac OS X plist files.
* [ ] poplib POP3 protocol client (requires sockets).
* [ ] \*_posix_- \[ ] (Unix) The most common POSIX system calls (normally used via module os).
* [ ] **pprint** Data pretty printer.
* [ ] **profile** Python source profiler.
* [ ] pstats Statistics object for use with the profiler.
* [ ] pty (Linux) Pseudo-Terminal Handling for Linux.
* [ ] pwd (Unix) The password database (getpwnam() and friends).
* [ ] **py\_compile** Generate byte-code files from Python source files.
* [ ] pyclbr Supports information extraction for a Python class browser.
* [ ] **pydoc** Documentation generator and online help system.

## q

* [ ] queue A synchronized queue class.
* [ ] quopri Encode and decode files using the MIME quoted-printable encoding.

## r

* [ ] **random** Generate pseudo-random numbers with various common distributions.
* [ ] **re** Regular expression operations.
* [ ] \*_readline_- \[ ] (Unix) GNU readline support for Python.
* [ ] reprlib Alternate repr() implementation with size limits.
* [ ] resource (Unix) An interface to provide resource usage information on the current process.
* [ ] rlcompleter Python identifier completion, suitable for the GNU readline library.
* [ ] **runpy** Locate and run Python modules without importing them first.

## s

* [ ] sched General purpose event scheduler.
* [ ] **secrets** Generate secure random numbers for managing secrets.
* [ ] select Wait for I/O completion on multiple streams.
* [ ] selectors High-level I/O multiplexing.
* [ ] shelve Python object persistence.
* [ ] **shlex** Simple lexical analysis for Unix shell-like languages.
* [ ] **shutil** High-level file operations, including copying.
* [ ] signal Set handlers for asynchronous events.
* [ ] site Module responsible for site-specific configuration.
* [ ] smtpd A SMTP server implementation in Python.
* [ ] smtplib SMTP protocol client (requires sockets).
* [ ] sndhdr Determine type of a sound file.
* [ ] socket Low-level networking interface.
* [ ] socketserver A framework for network servers.
* [ ] spwd (Unix) The shadow password database (getspnam() and friends).
* [ ] sqlite3 A DB-API 2.0 implementation using SQLite 3.x.
* [ ] ssl TLS/SSL wrapper for socket objects
* [ ] stat Utilities for interpreting the results of os.stat(), os.lstat() and os.fstat().
* [ ] statistics Mathematical statistics functions
* [ ] **string** Common string operations.
* [ ] stringprep String preparation, as per RFC 3453
* [ ] **struct** Interpret bytes as packed binary data.
* [ ] **subprocess** Subprocess management.
* [ ] sunau Provide an interface to the Sun AU sound format.
* [ ] symbol Constants representing internal nodes of the parse tree.
* [ ] symtable Interface to the compiler's internal symbol tables.
* [ ] **sys** Access system-specific parameters and functions.
* [ ] **sysconfig** Python's configuration information
* [ ] \*_syslog_- \[ ] (Unix) An interface to the Unix syslog library routines.

## t

* [ ] tabnanny Tool for detecting white space related problems in Python source files in a directory tree.
* [ ] **tarfile** Read and write tar-format archive files.
* [ ] telnetlib Telnet client class.
* [ ] **tempfile** Generate temporary files and directories.
* [ ] termios (Unix) POSIX style tty control.
* [ ] \- test Regression tests package containing the testing suite for Python.
* [ ] textwrap Text wrapping and filling
* [ ] **threading** Thread-based parallelism.
* [ ] **time** Time access and conversions.
* [ ] **timeit** Measure the execution time of small code snippets.
* [ ] \- tkinter Interface to Tcl/Tk for graphical user interfaces
* [ ] token Constants representing terminal nodes of the parse tree.
* [ ] tokenize Lexical scanner for Python source code.
* [ ] trace Trace or track Python statement execution.
* [ ] traceback Print or retrieve a stack traceback.
* [ ] tracemalloc Trace memory allocations.
* [ ] \*_tty_- \[ ] (Unix) Utility functions that perform common terminal control operations.
* [ ] turtle An educational framework for simple graphics applications
* [ ] turtledemo A viewer for example turtle scripts
* [ ] **types** Names for built-in types.
* [ ] **typing** Support for type hints (see :pep:`484`).

## u

* [ ] unicodedata Access the Unicode Database.
* [ ] \- unittest Unit testing framework for Python.
* [ ] \- urllib
* [ ] uu Encode and decode files in uuencode format.
* [ ] uuid UUID objects (universally unique identifiers) according to RFC 4122

## v

* [ ] **venv** Creation of virtual environments.

## w

* [ ] warnings Issue warning messages and control their disposition.
* [ ] wave Provide an interface to the WAV sound format.
* [ ] weakref Support for weak references and weak dictionaries.
* [ ] **webbrowser** Easy-to-use controller for Web browsers.
* [ ] winreg (Windows) Routines and objects for manipulating the Windows registry.
* [ ] winsound (Windows) Access to the sound-playing machinery for Windows.
* [ ] \- wsgiref WSGI Utilities and Reference Implementation.

## x

* [ ] xdrlib Encoders and decoders for the External Data Representation (XDR).
* [ ] \- xml Package containing XML processing modules
* [ ] \- xmlrpc

## z

* [ ] **zipapp** Manage executable Python zip archives
* [ ] **zipfile** Read and write ZIP-format archive files.
* [ ] **zipimport** Support for importing Python modules from ZIP archives.
* [ ] **zlib** Low-level interface to compression and decompression routines compatible with gzip.
