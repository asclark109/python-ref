## Python, bash (UNIX shell), powershell (windows powershell)

### Errors
Syntax Error: related to syntax/structure of the program. program halts as soon as pythong parses program

Runtime Error: error that only occurs while program is running 

Semantic (Logical) Error: program runs but does not do what is expected

### basics: bash (UNIX shell) commands
```shellscript

ls
cd
mv
mkdir
rmdir
man
touch
rm -i
clear
cp
which
whoami
```

### more: bash (UNIX shell) commands

| Bash      | Description 
| :---        |    :----   | 
| pwd	| print working directory |
| hostname	|my computer's network name|
| mkdir	|make directory|
| cd	|change directory|
| ls	|list directory|
| rmdir	|remove directory|
|rm -rf |	deletes it and all its contents
| pushd	|push directory|
| popd	|pop directory|
| cp	|copy a file or directory|
|cp -r |? copy file/directory and all its contents
| mv	|move a file or directory|
| less	|page through a file|
| cat	|print the whole file|
| xargs	|execute arguments|
| find	|find files|
| grep	|find things inside files|
| man	|read a manual page|
| apropos|	find which man page is appropriate|
| env	|look at your environment|
| echo	|print some arguments|
| export|	export/set a new environment variable|
| exit	|exit the shell|
| sudo	| DANGER! become super user root DANGER!|
| chmod |	change the access permissions of file system objects (files and directories) sometimes  known as modes |
|chown	| abbreviation of change owner, is used on Unix and Unix-like operating systems to change the owner of file system files, directories|
|tar	| https://www.howtogeek.com/248780/how-to-compress-and-extract-files-using-the-tar-command-on-linux/|

examples:

```bash
touch "myfile.txt"
cp myfile.txt ~/Documents/myfile.txt
cd ~/Documents/
pwd
ls
rm myfile.txt
echo $PATH
```

### more: Powershell (Windows Shell) commands

| Windows Shell | Description |
| :---        |    :----   | 
|pwd	|print working directory|
|hostname	|my computer's network name
|mkdir	|make directory
|cd	|change directory
|ls	|list directory
|rmdir	|remove directory
|pushd	|push directory
|popd	|pop directory
|cp	|copy a file or directory
|robocopy|	robust copy
|mv	|move a file or directory
|more	|page through a file
|type	|print the whole file
|forfiles	|run a command on lots of files
|dir -r	|find files
|select-string|	find things inside files
|help	|read a manual page
|helpctr	|find what man page is appropriate
|echo	|print some arguments
|set	|export/set a new environment variable
|exit	|exit the shell
|runas	|DANGER! become super user root DANGER!

### Escape Characters
|Escape	|What it does|
| :---        |    :----   | 
|\\	|Backslash (\) |
|\’	|Single-quote (‘)|
|\’’	|Double-quote (“)|
|\a	|ASCII bell (BEL)|
|\b	|ASCII backspace (BS)|
|\f	|ASCII formfeed (FF)|
|\n	|ASCII linefeed (LF)|
|\N{name}	|Character named name in the Unicode database (Unicode only)|
|\r	|Carriage return (CR)|
|\t	|Horizontal tab (TAB)|
|\uxxxx	|Character with 16-bit hex value xxxx|
|\Uxxxxxxxx	|Character with 32-bit hex value xxxxxxxx|
|\v	|ASCII vertical tab (VT)|
|\000	|Character with octal value 000|
|\xhh	|Character with hex value hh|

### bash: tar
creating archive file (compression optional)
```bash
Tar -cvf my_files.tar file* ex*.py
```
opening archive file
```bash
Tar -xvf my_files.tar
```

|param	|What it does|
| :---        |    :----   | 
|-c	|create|
|-v	|verbose|
|-f	|archive file name|
|-z	|compress|
|-x	|extract|

### Version nomenclature
```bash
3.9.5
```
|Escape	|What it does|
|   ---      |    ---   | 
first digit: | large revamps.
second digit:| feature additions.
last digit: |bug fixes.

## python: Variables, Expressions, Statements

built-in data types
```python
int       # numeric
long      # numeric
float     # numeric
complex   # numeric
str       # sequences (iterable, immutable, ordered)
bytes     # sequences (iterable)
tuple     # sequences (iterable, immutable, ordered)
dict      # sequences (iterable, mutable, unordered)
set       # sequences (iterable, mutable, unordered)
list      # sequences (iterable, mutable, ordered)
```

## keywords
```python
and         # A logical operator
as          # To create an alias
assert      # For debugging
break       # To break out of a loop
class       # To define a class
continue    # To continue to the next iteration of a loop
def         # To define a function
del         # To delete an object
elif        # Used in conditional statements, same as else if
else        # Used in conditional statements
except      # Used with exceptions, what to do when an exception occurs
False       # Boolean value, result of comparison operations
finally     # Used with exceptions, a block of code that will be executed no matter if there is an exception or not
for         # To create a for loop
from        # To import specific parts of a module
global      # To declare a global variable
if          # To make a conditional statement
import      # To import a module
in          # To check if a value is present in a list, tuple, etc.
is          # To test if two variables are equal
lambda      # To create an anonymous function
None        # Represents a null value
nonlocal    # To declare a non-local variable
not         # A logical operator
or          # A logical operator
pass        # A null statement, a statement that will do nothing
raise       # To raise an exception
return      # To exit a function and return a value
True        # Boolean value, result of comparison operations
try         # To make a try...except statement
while       # To create a while loop
with        # Used to simplify exception handling
yield       # To end a function, returns a generator
```

### reserved words
```python
and del for is raise
assert elif from lambda
return break else
global not try class
except if or while
continue exec import
pass yield def finally
in print as with
```

### notable built-in functions

```python
abs()
delattr()
hash()
memoryview()
set()
all()
dict()
help()
min()
setattr()
any()
dir()
hex()
next()
slice()
ascii()
divmod()
id()
object()
sorted()
bin()
enumerate()
input()
oct()
staticmethod()
bool()
eval()
int()
open()
str()
breakpoint()
exec()
isinstance()
ord()
sum()
bytearray()
filter()
issubclass()
pow()
super()
bytes()
float()
iter()
print()
tuple()
callable()
format()
len()
property()
type()
chr()
frozenset()
list()
range()
vars()
classmethod()
getattr()
locals()
repr()
zip()
compile()
globals()
map()
reversed()
import()
complex()
hasattr()
max()
round()	
```

|               |             |   built-ins  |              |                |
|:-------------:|:-----------:|:------------:|:------------:|:--------------:|
| abs()         | delattr()   | hash()       | memoryview() | set()          |
| all()         | dict()      | help()       | min()        | setattr()      |
| any()         | dir()       | hex()        | next()       | slice()        |
| ascii()       | divmod()    | id()         | object()     | sorted()       |
| bin()         | enumerate() | input()      | oct()        | staticmethod() |
| bool()        | eval()      | int()        | open()       | str()          |
| breakpoint()  | exec()      | isinstance() | ord()        | sum()          |
| bytearray()   | filter()    | issubclass() | pow()        | super()        |
| bytes()       | float()     | iter()       | print()      | tuple()        |
| callable()    | format()    | len()        | property()   | type()         |
| chr()         | frozenset() | list()       | range()      | vars()         |
| classmethod() | getattr()   | locals()     | repr()       | zip()          |
| compile()     | globals()   | map()        | reversed()   | \_\_import\_\_()   |
| complex()     | hasattr()   | max()        | round()      |                |


```python
abs()                 # Returns the absolute value of a number
all()                 # Returns True if all items in an iterable object are true
any()                 # Returns True if any item in an iterable object is true
ascii()               # Returns a readable version of an object. Replaces none-ascii characters with escape character
bin()                 # Returns the binary version of a number
bool()                # Returns the boolean value of the specified object
bytearray()           # Returns an array of bytes
bytes()               # Returns a bytes object
callable()            # Returns True if the specified object is callable, otherwise False
chr()                 # Returns a character from the specified Unicode code.
classmethod()         # Converts a method into a class method
compile()             # Returns the specified source as an object, ready to be executed
complex()             # Returns a complex number
delattr()             # Deletes the specified attribute (property or method) from the specified object
dict()                # Returns a dictionary (Array)
dir()                 # Returns a list of the specified object's properties and methods
divmod()              # Returns the quotient and the remainder when argument1 is divided by argument2
enumerate()           # Takes a collection (e.g. a tuple) and returns it as an enumerate object
eval()                # Evaluates and executes an expression
exec()                # Executes the specified code (or object)
filter()              # Use a filter function to exclude items in an iterable object
float()               # Returns a floating point number
format()              # Formats a specified value
frozenset()           # Returns a frozenset object
getattr()             # Returns the value of the specified attribute (property or method)
globals()             # Returns the current global symbol table as a dictionary
hasattr()             # Returns True if the specified object has the specified attribute (property/method)
hash()                # Returns the hash value of a specified object
help()                # Executes the built-in help system
hex()                 # Converts a number into a hexadecimal value
id()                  # Returns the id of an object
input()               # Allowing user input
int()                 # Returns an integer number
isinstance()          # Returns True if a specified object is an instance of a specified object
issubclass()          # Returns True if a specified class is a subclass of a specified object
iter()                # Returns an iterator object
len()                 # Returns the length of an object
list()                # Returns a list
locals()              # Returns an updated dictionary of the current local symbol table
map()                 # Returns the specified iterator with the specified function applied to each item
max()                 # Returns the largest item in an iterable
memoryview()          # Returns a memory view object
min()                 # Returns the smallest item in an iterable
next()                # Returns the next item in an iterable
object()              # Returns a new object
oct()                 # Converts a number into an octal
open()                # Opens a file and returns a file object
ord()                 # Convert an integer representing the Unicode of the specified character
pow()                 # Returns the value of x to the power of y
print()               # Prints to the standard output device
property()            # Gets, sets, deletes a property
range()               # Returns a sequence of numbers, starting from 0 and increments by 1 (by default)
repr()                # Returns a readable version of an object
reversed()            # Returns a reversed iterator
round()               # Rounds a numbers
set()                 # Returns a new set object
setattr()             # Sets an attribute (property/method) of an object
slice()               # Returns a slice object
sorted()              # Returns a sorted list
@staticmethod()       # Converts a method into a static method
str()                 # Returns a string object
sum()                 # Sums the items of an iterator
super()               # Returns an object that represents the parent class
tuple()               # Returns a tuple
type()                # Returns the type of an object
vars()                # Returns the __dict__ property of an object
zip()                 # Returns an iterator, from two or more iterators

```



### Operators
```python
**   # Exponent				2 ** 3 = 8
%	# Modulus/Remainder		22 % 8 = 6
//   # Integer division		22 // 8 = 2
/	# Division				22 / 8 = 2.75
*	# Multiplication		3 * 3 = 9
-	# Subtraction			5 - 2 = 3
+	# Addition				2 + 2 = 4
```

### Comparison Operators
```python
==	#Equal to
!=	#Not equal to
<	 #Less than
>	 #Greater Than
<=	#Less than or Equal to
>=	#Greater than or Equal to
```

### Boolean Operatoes
```python
True and True	   #True
True and False	  #False
False and True	  #False
False and False	 #False

True or True	    #True
True or False	   #True
False or True	   #True
False or False	  #False

not True	        #False
not False	       #True
```

### if, elif, else
control logic flow
```python
name = 'Bob'
age = 30
if name == 'Alice':
    print('Hi, Alice.')
elif age < 12:
    print('You are not Alice, kiddo.')
elif age < 16:
    print('You are not Alice, teen.')
else:
    print('You are neither Alice nor a little kid.')
```

### while, break, continue
while loops repeat until a condition becomes false.\
break can be used to break out of a loop iteration.\
continue can be used to immediately jump to the next iteration in a loop.

```python
spam = 0
while spam < 5:
    print('Hello, world.')
    spam = spam + 1
```


```python
while True:
    print('Who are you?')
    name = input()
    if name != 'Joe':
        continue
    print('Hello, Joe. What is the password? (It is a fish.)')
    password = input()
    if password == 'swordfish':
        break
print('Access granted.')
```

### functions
parameters: objects defined in a function header.\
arguments: objects passed into a function when invoking it.
```python

# parameters: name, name1, name2, name3
def say_personalized_hello(name):
	print("Hello " + name)
def say_personalized_hello(name1, name2, name3):
	print("Hello " + name1)
	print("Hello " + name2)
	print("Hello " + name3)

# arguments: "Jane", "Bob", "Lola"
say_personalized_hello("Jane")
say_personalized_hello("Jane","Bob","Lola")

# Void function with no arguments
def myFunction():
	print("Hello world")

# Function returning a value
def myFunction2():
	return "Hello world")

# Function taking argument and
# returning a value
def myFunction3(name):
	return "Hello world" + name)
```

functions automatically return None, unless specified to\
return something else.
```python

obj = say_personalized_hello("jane")
# obj points to None

def add_one(number):
	return number+1

new_num = add_one(4)
# new_num points to 5
```

can pass in variable position and keyword arguments with *argv, **kwargs convention:
```python
def function_var(par1, *argv, **kwargs):
	for item in argv:
		print(item)
	for key,item in kwargs.items():
		print(item)
```


### iteration
'for' loop to iterate through an iterable
```python
# for loop
for i in range(4):
	print(i)

# for loop
for item in num_list:
	print(item)
```

'while' looop to iterate until a condition is false
```python
n = 5
while n > 0:
	print n
	n = n - 1
print('Blastoff!')

# >>> 5
# >>> 4
# >>> 3
# >>> 2
# >>> 1
# >>> Blastoff!
```

Can use an else statement with a for loop with a break\
statement to do something if the for loop proceeds until\
the end.
```python
>>> for i in [1, 2, 3, 4, 5]:
>>>    if i == 3:
>>>        break
>>> else:
>>>    print("only executed when no item of the list is equal to 3")
```

### recursion
function that calls itself.\
needs to have base case and recursive case:\
\
advantage: conceptually easier to think about. elegant\
disadvantage: uses more memory. stackover flow error possible\
if function runs for too long.
```python
def countdown(n):
	# Test the current value of `n`
	if n < 0:
		print('Blastoff!')
	else:
		print("n = %s" % n)
		# Call countdown again
		countdown(n-1)

countdown(5)
# >>> 5 4 3 2 1 0 Blastoff!
```

### augmented assignment statements
```python
spam += 1		# spam = spam + 1
spam -= 1		# spam = spam - 1
spam *= 1		# spam = spam * 1
spam /= 1		# spam = spam / 1
spam %= 1		# spam = spam % 1
```

### importing modules
importing a module creates a .pyc file (compiled byte code to be\
interpreted by the Python VM)\
\
where python looks for importing:\
(1)	current directory\
(2)	python path (to figure this out…import sys, print(sys.path))

```python
import random               # access methods, objects in random with "random."
for i in range(5):
    print(random.randint(1, 10))

import random as r			# random now referenced by r
from module import randint  # can now reference randint() directly
from module import *        # can now reference everything in module without module.
```
When file runs as standalone, \_\_name\_\_ attribute gets set to '\_\_main\_\_'
```python
if __name__ == '__main__':
	main()
```
### packages
namespace containing more packages or modules\
namespace is a system to clearly define scope in a program. Prevents name clashing\
package requires \_\_init\_\_.py file in folder\
\_\_init\_\_.py can be blank\
One helpful thing you can do inside \_\_init\_\_.py is define the \_\_all\_\_ attribute, \
which takes a list of the modules you want to have imported when the whole package\
is import e.g. from package import *\
\
In example below international is a package (a folder), containing \_\_init\_\_.py,\
chinese.py, english.py, spanish.py
```python
# __init__.py
__all__ = ["chinese","english","spanish"]

# greeting.py
from international import *

chinese.say_hi()
english.say_hi()
spanish.say_hi()
```


### file anatomy
note: a 'shebang' (#!) specifies $PATH for Python interpreter\
Also used in other scripting languages (e.g. #!/usr/bin/perl)
```python
#!/usr/bin/env python                          #Shebang. first line

# docstring (usually on the second line)
"""this is my docstrong describing what this module is
this will be returned when someone calls help(my_module)""" 


# metadata
__author__ = 'Austin Clark'
__version__ = '1.0.0'

# import modules. 
# Good to import sys first.
# Then 3rd party
# Then use ones you wrote
import random


# declare global constants
# (If any) and use ALL_CAPS
MY_CONSTANT = 3.14

# Define main() function
# It’s a good idea to name main function main() because other developers will see it
def main():
	do_func()

# define (helper) functions


# boiler plate call to main to begin the program
if __name__ == '__main__':
	main()
```


### exception handling
try / except
```python
>>> def spam(divideBy):
>>>     try:
>>>         return 42 / divideBy
>>>     except ZeroDivisionError as e:
>>>         print('Error: Invalid argument: {}'.format(e))
```
(Less common) use of finally to do something in any event:\
try or except case
```python
>>> def spam(divideBy):
>>>     try:
>>>         return 42 / divideBy
>>>     except ZeroDivisionError as e:
>>>         print('Error: Invalid argument: {}'.format(e))
>>>     finally:
>>>         print("-- division finished --")
```
Can raise specific exceptions
```python
try:
	f = open('myfile.txt')
	s = f.readline()
	i = int(s.strip())
except OSError as err:
	print("OS error: {0}".format(err))
except ValueError:
	print("Could not convert data to an integer.")
except:
	print("Unexpected error:", sys.exc_info()[0])
```
Can use try, except, else, finally
```python
try:
	number = int(number_string)
except:
	# An exception is raised
	print("We couldn't convert the number to an integer.")
else:
	# No exception was raised
	number *= 2
	print(f"The number doubled is {number}")
finally:
	# This happens no matter what
	print("-- Done --")
```

### strings
```python
capitalize()	 # Converts the first character to upper case
casefold()	   # Converts string into lower case
center()	     # Returns a centered string
count()	      # Returns the number of times a specified value occurs in a string
encode()	     # Returns an encoded version of the string
endswith()	   # Returns true if the string ends with the specified value
expandtabs()	 # Sets the tab size of the string
find()	       # Searches the string for a specified value and returns the position of where it was found
format()	     # Formats specified values in a string
format_map()	 # Formats specified values in a string
index()	      # Searches the string for a specified value and returns the position of where it was found
isalnum()	    # Returns True if all characters in the string are alphanumeric
isalpha()	    # Returns True if all characters in the string are in the alphabet
isdecimal()	  # Returns True if all characters in the string are decimals
isdigit()        # Returns True if all characters in the string are digits
isidentifier()   # Returns True if the string is an identifier
islower()	    # Returns True if all characters in the string are lower case
isnumeric()	  # Returns True if all characters in the string are numeric
isprintable()    # Returns True if all characters in the string are printable
isspace()	    # Returns True if all characters in the string are whitespaces
istitle()	    # Returns True if the string follows the rules of a title
isupper()        # Returns True if all characters in the string are upper case
join()           # Joins the elements of an iterable to the end of the string
ljust()          # Returns a left justified version of the string
lower()          # Converts a string into lower case
lstrip()     	# Returns a left trim version of the string
maketrans()      # Returns a translation table to be used in translations
partition()      # Returns a tuple where the string is parted into three parts
replace()        # Returns a string where a specified value is replaced with a specified value
rfind()          # Searches the string for a specified value and returns the last position of where it was found
rindex()         # Searches the string for a specified value and returns the last position of where it was found
rjust()          # Returns a right justified version of the string
rpartition()	 # Returns a tuple where the string is parted into three parts
rsplit()     	# Splits the string at the specified separator, and returns a list
rstrip()	     # Returns a right trim version of the string
split()          # Splits the string at the specified separator, and returns a list
splitlines()     # Splits the string at line breaks and returns a list
startswith()     # Returns true if the string starts with the specified value
strip()	      # Returns a trimmed version of the string
swapcase()   	# Swaps cases, lower case becomes upper case and vice versa
title()	      # Converts the first character of each word to upper case
translate()  	# Returns a translated string
upper()	      # Converts a string into upper case
zfill()	      # Fills the string with a specified number of 0 values at the beginning
```

string formatting:
```python
'%s %s' % ('one', 'two')    # one two
'%10s' % ('test',)          # " test"
'%-10s' % ('test',)         # "test "
'%.3f' % (3.1415927,)       # 3.142
'%06.2f' % (3.1415927,)     # 003.14

name = 'harry'
day = 'thursday'
'hello, Mr. {0}! How goes it on this {1}'.format(name,day)

>>>
```

### list

lists require more memory than tuples, but are mutable.\
lists created, indexed, and concatenated like so:
```python
my_list = [1,2,'apple']
apple_string = my_list[2]
nums = my_list[0:2]
nums = my_list[-1]			#index backwards: last element
nums = my_list[:]			#index all elements
bigger_list = my_list + [5,6]
```
list methods:
```python
append()     # Adds an element at the end of the list
clear()      # Removes all the elements from the list
copy()       # Returns a copy of the list
count()      # Returns the number of elements with the specified value
extend()     # Add the elements of a list (or any iterable), to the end of the current list
index()      # Returns the index of the first element with the specified value
insert()     # Adds an element at the specified position
pop()        # Removes the element at the specified position
remove()     # Removes the first item with the specified value
reverse()    # Reverses the order of the list
sort()       # Sorts the list
```
can use sorted(), which returns a copy of an iterable sorted,\
or can use list.sort(), which sorts the list in place.\
Use reverse=True parameter for sort() to sort in reverse direction\
\
\
common functions with lists:
```python
del
append()
extend()
sort()       #-- sorts in place
sorted()     #-- (built in) gives new list
insert()
pop()
remove()
```

### dict
dict methods
```python
clear()      # Removes all the elements from the dictionary
copy()       # Returns a copy of the dictionary
fromkeys()   # Returns a dictionary with the specified keys and value
get()        # Returns the value of the specified key
items()      # Returns a list containing a tuple for each key value pair
keys()       # Returns a list containing the dictionary's keys
pop()        # Removes the element with the specified key
popitem()    # Removes the last inserted key-value pair
setdefault() # Returns the value of the specified key. If the key does not exist: insert the key, with the specified value
update()     # Updates the dictionary with the specified key-value pairs
values()     # Returns a list of all the values in the dictionary
```
common methods include:
```python
dict.get(idx,defaultvalue)
keys()
values()
items()
```
looping over a dict:
```python
>>> for key, value in a_dict.items():
...     print(key, '->', value)
...
color -> blue
fruit -> apple
pet -> dog
```


### Tuple
Tuples are like lists, but they require less memory (as they are immutable)
created, indexed like so:
```python
my_tuple = (1,2,3,4,'apple')
apple_str = my_tuple[4]
```
methods for tuple
```python
count()	  # Returns the number of times a specified value occurs in a tuple
index()	  # Searches the tuple for a specified value and returns the position of where it was found
```

### built-in exceptions
```python
ArithmeticError          # Raised when an error occurs in numeric calculations
AssertionError           # Raised when an assert statement fails
AttributeError           # Raised when attribute reference or assignment fails
Exception                # Base class for all exceptions
EOFError                 # Raised when the input() method hits an "end of file" condition (EOF)
FloatingPointError       # Raised when a floating point calculation fails
GeneratorExit            # Raised when a generator is closed (with the close() method)
ImportError              # Raised when an imported module does not exist
IndentationError         # Raised when indendation is not correct
IndexError               # Raised when an index of a sequence does not exist
KeyError                 # Raised when a key does not exist in a dictionary
KeyboardInterrupt        # Raised when the user presses Ctrl+c, Ctrl+z or Delete
LookupError              # Raised when errors raised cant be found
MemoryError              # Raised when a program runs out of memory
NameError                # Raised when a variable does not exist
NotImplementedError      # Raised when an abstract method requires an inherited class to override the method
OSError                  # Raised when a system related operation causes an error
OverflowError            # Raised when the result of a numeric calculation is too large
ReferenceError           # Raised when a weak reference object does not exist
RuntimeError             # Raised when an error occurs that do not belong to any specific expections
StopIteration            # Raised when the next() method of an iterator has no further values
SyntaxError              # Raised when a syntax error occurs
TabError                 # Raised when indentation consists of tabs or spaces
SystemError              # Raised when a system error occurs
SystemExit               # Raised when the sys.exit() function is called
TypeError                # Raised when two different types are combined
UnboundLocalError        # Raised when a local variable is referenced before assignment
UnicodeError             # Raised when a unicode problem occurs
UnicodeEncodeError       # Raised when a unicode encoding problem occurs
UnicodeDecodeError       # Raised when a unicode decoding problem occurs
UnicodeTranslateError    # Raised when a unicode translation problem occurs
ValueError               # Raised when there is a wrong value in a specified data type
ZeroDivisionError        # Raised when the second operator in a division is zero
```

### user input
```python
input()	  # beckons 
index()	  # Searches the tuple for a specified value and returns the position of where it was found
```

### file methods

Structured (csv, XML, JSON, HTML)\
Text (.txt)\
Binary (.docx, .sql) special created by application…usually specific to application. Saved as bin of 1’s and 0’s\
Main considerations: size, privacy, human readable


```python
close()         # Closes the file
detach()        # Returns the separated raw stream from the buffer
fileno()        # Returns a number that represents the stream, from the operating system's perspective
flush()         # Flushes the internal buffer
isatty()        # Returns whether the file stream is interactive or not
read()          # Returns the file content
readable()      # Returns whether the file stream can be read or not
readline()      # Returns one line from the file
readlines()     # Returns a list of lines from the file
seek()          # Change the file position
seekable()      # Returns whether the file allows us to change the file position
tell()          # Returns the current file position
truncate()      # Resizes the file to a specified size
writable()      # Returns whether the file can be written to or not
write()         # Writes the specified string to the file
writelines()    # Writes a list of strings to the file
```

boiler plate code for reading files:
```python
try:
	with open('file.txt', 'r')	#open returns a “handle”
		for line in f:
			Print(line)
except:
	print('had trouble reading file')
```
Use split, strip, lstrip, rsplit to handle whitespace in reading files.\
split() separates by whitespace
```python
try:
	with open('file.txt', 'r')	#open returns a “handle”
		for line in f:
    		clean_line = line.strip()
    		clean_line = clean_line.lower()
    		print(clean_line)
except:
	print('had trouble reading file')
```
adding to files:
```python
try:
	with open('file.txt', 'a')	#open returns a “handle”
		f.write("hello world\n")
except:
	print('had trouble reading file')
```
Split, strip, lstrip, rsplit to handle whitespace in reading files
Split() separates by whitespace, or a different character specified by sep= parameter


### common modules

```python
# misc
import random       # random.randint(0,100) for random ints
                    # random.choice([1,2,3])
import datetime     # useful for dates and time

today = datetime.date.today()
print('Today :', today)
one_day = datetime.timedelta(days=1)
print('One day :', one_day)
yesterday = today - one_day
print('Yesterday:', yesterday)
# Today : 2017-01-22
# One day : 1 day, 0:00:00
# Yesterday: 2017-01-21

# text
import string
import textwrap
import re			# regular expressions!
import difflib

# data structures
import collections  # has useful grouping functions and types
import enum
import array
import heapq
import bisect
import queue
import struct
import weakref
import copy
import pprint

# algorithms
import functools
import itertools    # powerful ways to iterate through iterables
                    # itertools.count()
					# itertools.permutations(['a','b','c'])
					# itertools.combinations(['a','b','c'],2)
					# itertools.combinations(['abc'],2)
```

### os module
```python
import os
dir(os)                  # operating system
os.getcwd()
os.cwd()                 # current working directory-
os.path.abspath()        # gets absolute path of file
os.path.isdir()          # says whether this is a directory
os.path.listdir()        # tells you all files in path
os.path.join(root,file)		

>>> os.cwd()
# /Users/tbinkowski/Google Drive/g-Teaching/uchicago.codes/
lectures/session4
>>> os.path.abspath('c.py')
# /Users/tbinkowski/Google Drive/g-Teaching/uchicago.codes/
lectures/session4/c.py
>>> os.path.isdir('../')
# True
>>> os.listdir('./')
# ['workspace.py', 'writing_files.py']
```

### command line arguments
```python
import sys

# command line arguments stored in sys.argv
# sys.argv[0] holds the name of the script.
sys.argv
```

### global variables
```python
def myfunc():
	global x
	x = "fantastic"

myfunc()

print("Python is " + x)
```

### map, filter, reduce
map applies a function to every element in iterable, making a map object:
```python
>>>ls = ['1','2','3']
>>>ls_int = list(map(int,ls))
>>>ls_int
[1, 2, 3]
```
filter() forms a new list that contains only elements that satisfy a certain
condition, i.e. the function we passed returns True.
```python
>>>def starts_with_A(s):
>>>    return s[0] == "A"

>>>fruit = ["Apple", "Banana", "Pear", "Apricot", "Orange"]
>>>filter_object = filter(starts_with_A, fruit)

>>>print(list(filter_object))
['Apple', 'Apricot']
```
reduce is no longer a built-in but rather exists in the functools module
reduce() is a bit harder to understand than map() and filter(),\
so let's look at a step by step example:\
\
We start with a list [2, 4, 7, 3] and pass the add(x, y) function\
to reduce() alongside this list, without an initial value\
\
reduce() calls add(2, 4), and add() returns 6\
\
reduce() calls add(6, 7) (result of the previous call to add() and\
the next element in the list as parameters), and add() returns 13\
\
reduce() calls add(13, 3), and add() returns 16\
\
Since no more elements are left in the sequence, reduce() returns 16\
```python
>>>from functools import reduce

>>>def add(x, y):
>>>    return x + y

>>>list = [2, 4, 7, 3]
>>>print(reduce(add, list))
16
```

### dir, help
dir() tells you about functions and attribute associated with object.\
```python
>>>dir(print)
['__call__', '__class__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__', '__lt__', '__module__', '__name__', '__ne__', '__new__', '__qualname__', '__reduce__', '__reduce_ex__', '__repr__', '__self__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', '__text_signature__']

```
help() tells you more about how to use that function/object: used to\
display the documentation of modules, functions, classes, keywords etc
```python
>>>help(print)
Help on built-in function print in module builtins:
print(...)
    print(value, ..., sep=' ', end='\n', file=sys.stdout, flush=False)

    Prints the values to a stream, or to sys.stdout by default.
    Optional keyword arguments:
    file:  a file-like object (stream); defaults to the current sys.stdout.
    sep:   string inserted between values, default a space.
    end:   string appended after the last value, default a newline.
    flush: whether to forcibly flush the stream.
```


### assertions, Pytest
assertions are a method of defensive programming and can be used for
making script tests with pytest
```python
# typical anatomy of test file
# has name: test_mymodule.py
import pytest
import mymodule

def test_func1():
	# testing for functionality
	assert mymodule.func1(1,1) == 2

	# testing for exceptions:
	with pytest.raises(Exception):
		mymodule.func1(-1,'apple')
```

can use commandline arguments with pytest:
```bash
pytest test_*.py
pytest tests/
pytest -k test_name
```

### regular expressions regex

```php
abc…        // Letters
123…        // Digits
\d          // Any Digit
\D          // Any Non-digit character
.           // Any Character
\.          // Period
[abc]       // Only a, b, or c
[^abc]      // Not a, b, nor c
[a-z]       // Characters a to z
[0-9]       // Numbers 0 to 9
\w          // Any Alphanumeric character
\W          // Any Non-alphanumeric character
{m}         // m Repetitions
{m,n}       // m to n Repetitions
*           // Zero or more repetitions
+           // One or more repetitions
?           // Optional character
\s          // Any Whitespace
\S          // Any Non-whitespace character
^…$         // Starts and ends
(…)         // Capture Group
(a(bc))     // Capture Sub-group
(.*)        // Capture all
(abc|def)   // Matches abc or def
```

In python, handled with re package\
\
Use re.search() to see if a string matches a regular expression
(Similar to find() from str built-in methods)\
\
Use re.findall() to extract portions of a string that match your regular\
expression.
```python
import re

saying = "One fish, two fish, red fish blue fish. This one has a
little star, this one has a little car. Say, what alot of fish
there are."
if re.search('fish', saying):
	print("Found the fish")

if saying.find('wish'):
	print("Found it")

if re.search('fish', saying):
	print("Found the fish")

# Return all matches
print re.findall('fish',saying)
# >>> ['fish', 'fish', 'fish', 'fish', 'fish']

match = re.search(r'\d\d\d', 'p123g')
print match.group() # "123"
# Greedy match
match = re.search(r'\d+', 'p123g')
print match.group() # "123"
match = re.search(r'\d{5}', 'p123456789g')
print match.group() # "12345"
match = re.search(r'\w\w\w', '@@abcd!!')
print match.group() # 'abc'
match = re.search(r'\w{4}', '@@abcd!!')
print match.group() # 'abcd'
match = re.search(r'(\d\w){3}', '1a2a3a4a5a')
print match.group() # 1a2a3a

regex = r"([a-zA-Z]+) (\d+)"
match = re.search(regex, "June 24")
print(("Match at index %s, %s" % (match.start(), match.end())))
# So this will print("June 24"
print(("Full match: %s" % (match.group(0))))
# So this will print("June"
print(("Month: %s" % (match.group(1))))
# So this will print("24"
print(("Day: %s" % (match.group(2))))
```