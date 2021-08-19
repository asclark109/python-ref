- [bash (UNIX shell), powershell (windows powershell)](#bash--unix-shell---powershell--windows-powershell-)
    + [basics: bash (UNIX shell) commands](#basics--bash--unix-shell--commands)
    + [more: bash (UNIX shell) commands](#more--bash--unix-shell--commands)
    + [more: Powershell (Windows Shell) commands](#more--powershell--windows-shell--commands)
    + [Escape Characters](#escape-characters)
    + [bash: tar](#bash--tar)
- [Python](#python)
    + [Errors](#errors)
    + [Version nomenclature](#version-nomenclature)
    + [Variables, Expressions, Statements](#variables--expressions--statements)
    + [keywords](#keywords)
    + [reserved words](#reserved-words)
    + [notable built-in functions](#notable-built-in-functions)
    + [Operators](#operators)
    + [Comparison Operators](#comparison-operators)
    + [Boolean Operatoes](#boolean-operatoes)
    + [if, elif, else](#if--elif--else)
    + [while, break, continue](#while--break--continue)
    + [iteration (for loop)](#iteration--for-loop-)
    + [functions](#functions)
    + [recursion](#recursion)
    + [augmented assignment statements](#augmented-assignment-statements)
    + [importing modules](#importing-modules)
    + [packages](#packages)
    + [file anatomy](#file-anatomy)
    + [exception handling](#exception-handling)
    + [strings](#strings)
    + [list](#list)
    + [dict](#dict)
    + [Tuple](#tuple)
    + [built-in exceptions](#built-in-exceptions)
    + [user input](#user-input)
    + [file methods](#file-methods)
    + [common modules](#common-modules)
    + [os module](#os-module)
    + [command line arguments](#command-line-arguments)
    + [global variables](#global-variables)
    + [map, filter, reduce](#map--filter--reduce)
    + [dir, help](#dir--help)
    + [assertions, Pytest](#assertions--pytest)
    + [regular expressions regex](#regular-expressions-regex)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>




# bash (UNIX shell), powershell (windows powershell)


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

```bash
pwd         # print working directory
hostname    #my computer's network name|
mkdir       #make directory|
cd          #change directory|
ls          #list directory|
rmdir       #remove directory|
rm -rf      #deletes it and all its contents
pushd       #push directory|
popd        #pop directory|
cp          #copy a file or directory|
cp -r       #? copy file/directory and all its contents
mv          #move a file or directory|
less        #page through a file|
cat         #print the whole file|
xargs       #execute arguments|
find        #find files|
grep        #find things inside files|
man         #read a manual page|
apropos     #find which man page is appropriate|
env         #look at your environment|
echo        #print some arguments|
export      #export/set a new environment variable|
exit        #exit the shell|
sudo        #DANGER! become super user root DANGER!|
chmod       #change the access permissions of file system objects (files and directories) sometimes  known as modes |
chown       #abbreviation of change owner, is used on Unix and Unix-like operating systems to change the owner of file system files, directories|
tar         #https://www.howtogeek.com/248780/how-to-compress-and-extract-files-using-the-tar-command-on-linux/|
```

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

```commandline
pwd            # print working directory|
hostname       # my computer's network name
mkdir          # make directory
cd             # change directory
ls             # list directory
rmdir          # remove directory
pushd          # push directory
popd           # pop directory
cp             # copy a file or directory
robocopy       # robust copy
mv             # move a file or directory
more           # page through a file
type           # print the whole file
forfiles       # run a command on lots of files
dir -r         # find files
select-string  # find things inside files
help           # read a manual page
helpctr        # find what man page is appropriate
echo           # print some arguments
set            # export/set a new environment variable
exit           # exit the shell
runas          # DANGER! become super user root DANGER!
```

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

# Python

### Errors
Syntax Error: related to syntax/structure of the program. program halts as soon as pythong parses program

Runtime Error: error that only occurs while program is running 

Semantic (Logical) Error: program runs but does not do what is expected


### Version nomenclature
```bash
3.9.5
```
|Escape	|What it does|
|   ---      |    ---   | 
first digit: | large revamps.
second digit:| feature additions.
last digit: |bug fixes.

### Variables, Expressions, Statements

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

### keywords
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

### iteration (for loop)
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
>>>'%s %s' % ('one', 'two')    # one two
>>>'%10s' % ('test',)          # " test"
>>>'%-10s' % ('test',)         # "test "
>>>'%.3f' % (3.1415927,)       # 3.142
>>>'%06.2f' % (3.1415927,)     # 003.14

>>>name = 'harry'
>>>day = 'thursday'
>>>'hello, Mr. {0}! How goes it on this {1}'.format(name,day)
'hello, Mr. harry! How goes it on this thursday'

>>>''.join(['abc','d','efg'])
'abcdefg'
```

```python
>>>for x in numbers:
>>>    print "{:10.4f}".format(x)
   23.2300
    0.1233
    1.0000
    4.2230
 9887.2000
```
The format specifier inside the curly braces follows the Python format string syntax.\ Specifically, in this case, it consists of the following parts:

The empty string before the colon means "take the next provided argument to format()" – in this 
case the x as the only argument.

The 10.4f part after the colon is the format specification.

The f denotes fixed-point notation.

The 10 is the total width of the field being printed, lefted-padded by spaces.

The 4 is the number of digits after the decimal point.


### list

lists require more memory than tuples, but are mutable.\
lists created, indexed, and concatenated like so:
```python
my_list = [1,2,'apple']
apple_string = my_list[2]
nums = my_list[0:2]
nums = my_list[-1]			# index backwards: last element
nums = my_list[:]			# index all elements
bigger_list = my_list + [5,6]
my_list[::-1]               # reverse list by indexing backwards
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
Tuples are like lists, but they require less memory (as they are immutable)\
They are created, indexed like so:
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
input()	  # beckons user for input
```

boiler-plate code for taking input from user:
```python
while True
	try:
		user_input = input('enter a number: ')
		numeric = float(user_input)
		break
	except
		print('that is not a valid number')
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
	 with open('file.txt', 'r') as f:	#open returns a “handle”
		for line in f:
			print(line)
except:
	print('had trouble reading file')
```
Use split, strip, lstrip, rsplit to handle whitespace in reading files.\
split() separates by whitespace
```python
try:
	with open('file.txt', 'r') as f:	#open returns a “handle”
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
	with open('file.txt', 'a') as f:	#open returns a “handle”
		f.write("hello world\n")
except:
	print('had trouble reading file')
```
Split, strip, lstrip, rsplit to handle whitespace in reading files\
Split() separates by whitespace, or a different character specified by sep= parameter\

```python
'r'      # Open for reading (default)
'w'      # Open for writing, truncating (overwriting) the file first
'a'      # Open for appending
'rb'     # Open in binary mode (read using byte data) 
'wb'     # Open in binary mode (read using byte data)
```

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


### Module 5: OOP

<ins>Structured programming</ins>: control flow (e.g. if/else) with repetition (e.g. for,while)\
\
<ins>procedural programming</ins>: problem broken in to sub-problems; still step-by-step iterations (sometimes "spaghetti" code)\
\
hallmark of procedural: use of functions to solve sub-problems, uses of global/local variables to store data, use of parameters to pass data to functions/procedures\
\
<ins>Object-oriented programming</ins>: organize functions/procedures with their required data into a single unit ("object").\
\
advantages of OO: reduce code duplication, resuability, manage large programs, natural fit for data and procedures.\
\
sometimes, the programming tasks might suggest that just a simple structural paradigm might suffice; a more complicated task involving data and procedures close together might suggest OO is a better approach.\

### Object-oriented programming

<ins>Object</ins>: self-contained code (method) and properties (data)\
\
Benefit of OO: abstraction. hides un-needed detail from other parts of the code\
\
Objects have properties and methods\
\
property: attribute or state\
method: do something (function & procedure)\

## Class

<ins>Class</ins>: defines abstract characteristics of an object.\
\
Notably, properties and methods.\
\
Class is the blueprint for a user-defined type\
\
e.g.
```python
class: Dog
	# attributes: name, color
	# methods: bark,roll_over
```

An <ins>object</ins> is an instance of a class

```Python
class Person:
	"""A class to hold contact info."""
	pass

# create instance
# the capital "P" lets user know that Person is a class, so we are creating an instance of a class
p = Person()

print(p)
# <__main__>.Person instance at 0x102449b00>
```

An "<ins>instance</ins>" is the object of a class created at runtime

Its "<ins>state</ins>" is the value of the attributes.

### (Class) attributes 

Classes can have instance variables and class variables

<ins>instance variable</ins>: holds values for a specific instance of the class

In python, there's no way to explicitly define instance variables.

```python
class Cat:
	def speak(self):
		print('meow')
	# ...

c = Cat()
# e.g. create an instance variable
c.name = "Lola"
```
In other languages you can explicitly define instance variables. Because of this, it's good to list the attributes in the docstrong of the class in Python

```python
class Dog:
	"""Represents man's best friends. Dogs 
	have the following roperties:    
	
	Attributes:
	     name: A string representing the name 
		 color: A string representing the Color 
		 age: An int representing the age
	"""

d = Dog()
d.name = "Fido"
d.color = "white and black"
d.age = 5
```

<ins>class variable</ins>: belongs to the class. holds values that are the same (static) for every class.\
\
class variables do not need an instance of a class to exist to be called\

```python
class Dog:
	"""Represents...

	Attributes:
	     name: A string representing the name 
		 color: A string representing the Color 
		 age: An int representing the age
	"""
	# Class variable representing legs
	legs = 4

	def bark(self):
		print('ruff')
```

### (Class) methods

A class has 'methods' that can act on an instance of it\
\
Functions only available to a class' instance\
\
also called 'messages' in somoe programming languages\
\
In Python, the ```self``` variable contains information about the specific instance of the class

```python
class Person:

	def say_greeting(self):
		print('hello')

	def say_something(self,msg):
		print(msg)

p = Person()
p.say_greeting()
p.say_something('hi')
```

can use dir() obtain all attributes/methods of a class

```python
>>> dir(list)
['__add__', '__class__', '__class_getitem__', '__contains__', '__delattr__', '__delitem__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__gt__', '__hash__', '__iadd__', '__imul__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__rmul__', '__setattr__', '__setitem__', '__sizeof__', '__str__', '__subclasshook__', 'append', 'clear', 'copy', 'count', 'extend', 'index', 'insert', 'pop', 'remove', 'reverse', 'sort']
```

In python, can declare class methods as a staticmethod or classmethod with decorators:

<ins>@staticmethod</ins>: works without an instance of the class

<ins>@classmethod</ins>: works with the class object

```python
class Dog:

	size = 'small'

	@staticmethod
	def bark():
		print('ruff')

	@classmethod
	def is_great_dane(cls):
		return cls.size == 'big'
```

### Object Lifecycle

Objects are created, used and destroyed during a program. Built-in methods to run when is created (constructor) and destroyed (destructor).\
\
Python has a special method that is called when an object is intitialized ```__init__```. Can override it to customize behavior.\
\
Can also override the ```__del__``` method, but usually you do not explicitly call this method. Python automatically handles memory and deletion of objects.

```python
class Dog:
	latin_name="Canis lupus familiaris"
	
	def __init__(self,name):
		self.name=name
		
d=Dog('Fido')
e=Dog('Snoopy')
```

### standard methods

Python has standard object methods that are sometimes useful to override:

```python
__init__(self, ...)
# This method is called just before the newly #created object is returned for usage. 
__del__(self)
# Called just before the object is destroyed (which has unpredictable timing,so avoid  using this)
__str__(self)
# Called when we use the print function or when str() is used. 
__lt__(self,other)
# Called when the less than operator (<) is used. Similarly, there are special methods for all the operators (+, >, etc.)
__getitem__(self,key)
#Called when x[key] indexing operation is used. 
__len__(self)
#Called when the built-in len() function is used for the sequence object.
```

### class inheritence

OOP promotes code reuse through "inheritance".\
\
Inheritance: process where a child class derives the attributes and methods from a parent class.\
\
"parent class" also called: base class, super class.\
"child class" also called: subclass,derived  class\

```python
class Parent:
	# attributes
	# methods

class Child(Parent):
	# Parent attributes
	# Parent methods

	# childs attributes
	# childs methods
```
Inheritance can be useful to model real-world relationships/hierarchies.\
\
e.g.
```
Parent: Animal
Child: Dog, Cat, Rabbit

Parent: Person
Child: Student, Teacher
```
Inheritance can be overkill. Think about benefits/costs. Consider whether inheritance is actually providing benefits:\
\
e.g.
```
Parent: Item
Child: Car, Bread, Skate
```
It is possible to have multiple levels of inheritance, but it is difficult to get right (i.e. inheriting from 2 super classes).

### Abstract Class

It's not uncommon to declare a base class that will never be used directly. This is called an "Abstract Class".\
\
e.g.
```
class: Vehicle
subclasses: car, truck, motorcycle,...
```

### Networking

<ins>Networking</ins>: interconnection of multiple devices connected using multiple paths for the purpose of sending/receiving data or media.\
\
Modern languages will have established practices/code/libraries for communication with other computers.\
\
Most difficulties will be related to efforts:
```
signal:         do you have good connection to internet?
connection:     connection type? 5G or dialup modem?
API: 
Servers:        server down?
...
```

<ins>HTTP</ins> is an agreed upon protocol for requesting/responding, sending/retreiving data.\
\
It's not only way to send data, but it is probably the most popular. This is because HTML is probably the most popular way to send data on the web, which uses HTTP; hence, why HTML is the most used protocol for the web.\
\
Other data formats: text, XML, JSON, binary,...\
\
Services have an <ins>Application Programming Interface (API)</ins> that they specify how others can use their data.\
\
User of an API is a "<ins>consumer</ins>".\
\
Many technologoies that support services:\
\
<ins>REST</ins>: Representational State Transfer\
<ins>SOAP</ins>: Simple Object Access Protocol\
\
REST, SOAP, implemented by practice. REST, SOAP, can be seen as agreed upon practices.\
\
e.g. Google Maps API
```
HTTP://MAPS.GOOGLEAPIS.COM/MAPS/API/GEOCODE/JSON?SENSOR=FALSE&ADDRESS=CHICAGO%2C+MI
```

The bad stuff:
```
ISO 8601 Date/Time Format   # not all web services use the same date/time format
Authentication              # as consumer of API, can be a bit of work to establish authentication (add level of complexity to working with web services)
Rate Limits                 # serivce might have rate limits
Payment                     # usually free quota, but use of large scale requires payment
```

Web browsers read and parse HTML to present it more cleanly.\
\
XML is used mostly for data transportation. It usually meant to be fed into another application; hence, not usually rendered for visualization like HTML. Typically, XML is considered verbose and overkill for most uses.\
\
JSON: JavaScript Object Notation. Now, it is used everywhere and is considered the standard way to share text based data. JSON data pretty easy to parse with Python.\
\
JSON is a syntax for storing and exchanging data. It works great in Python. Take a look at the ```json``` standard library in python.
```python
import json
data='''{
	"name" : "Mickey Mouse",
	"phone" : {
		"type" : "intl",
		"number" : "+1 734 303 4456"
	},
	"email" : {
		"hide" : "mickey@disney.com"
	}
}'''
	
info=json.loads(data)
# json.loads() converted str json data to dict

print'Name:',info["name"]
print'Hide:',info["email"]["hide"]
```

bringing in data:
```python
import json
data = {
	"number":1,
	"name":"Mickey Mouse"
	}

# load to JSON data
info=json.dumps(data)

print type(info["number"])
```

### Networking Modules

To request a response from the server, there are mainly two methods:
<ins>GET</ins>: to request data from server\
<ins>POST</ins>: to submit data to be processed to the server\
\
Most popular networking modules in python:
```
httplib
requests (most popular)
urllib
```

e.g.
```python
import requests
import json

url='https://....'
r=requests.get(url)

json_data=r.json()

for item in json_data:
	# parse away
```

e.g. requesting repos from GitHub
```python
import requests
import json

url="https://api.github.com/repos/.../issues?state=all&per_page=10"

r=requests.get(url)

for item in r.json():
	print("> ",item["title"],item["user"]["login"])

message=r.json()
```

e.g. request location from google maps API
```python
import requests 

# api-endpoint
URL="http://maps.googleapis.com/maps/api/geocode/json"

# location given here
location="chicago"

# Params dict for the parameters to be sent to the API
PARAMS= {'address':location}

# sending get request and saving the response
# as response object 
r=requests.get(url=URL,params=PARAMS)

# extracting data in json format
data=r.json()
```
JSON reults are a dictionary with keys.


### Algorithm Analysis

<ins>Algorithm</ins>: step-by-step instructions to solve a problem (not a program). An algorithm should be "robust"; i.e., solve the problem for all sets of inputs and outputs, handle all error conditions, and be deterministic (same output for same set of inputs)\

<ins>Program</ins>: implementation of an algorithm (in a programming language). In fact, may use many algorithms\

<ins>Correctness</ins>:  algorithm provides correct solution to the problem

<ins>Efficiency</ins>: two types \
Time: how long does it take to solve problem\
space: how much memory is needed?

Benchmarking vs analysis (i.e. real world performance): consider best case scenario, worst case scenario, and also average performance.

Consider also: ease of understanding, program maintenance, elegance.

Might be many different algorithms that solve the same probelm. how to measure what the "best" algorithm might be?:\

<ins>running time</ins>: very hardward dependent. not a great measure. Implementation details might vary (i.e. different implementations of the same algorithms. It'd be best to have a metric that is agnostic to these facts.\

<ins>Number of steps</ins>: if an algorithm is just a procedure consisting of a number of steps, then we can just count the number of steps.

<ins>Algorithm Analysis</ins>: concerned with comparing algorithms based upon the amount of computing resources that each algorithm uses (time, money: e.g. cloud computing services?, or even human resources: e.g. could pay 10 best computer scientist to spend a year to develop an incredible algorithm, but need to pay them for their time...was the algorithm worth the salary/time cost of developing the algorithm? So, more factors to consider than cost of literal computing resources).\

e.g. 3 different algorithms for removing elements of a list holding a "0":

|	| Space | Time |
| :---        |    :----   |  :----   | 
| Shuffle Left  | constant  | go through list many times | 
| Copy Over	| double | go through list once |
| Converging Pointers	|  constant | go through list once |

Measuring Efficieny: could time the program, but that depends on machine speed and thus is not very meaningful more globally, so it is better to count the steps of the program/algorithm. Ask the question: "how many 'fundamental steps' does the algorithm take"?\

Runtime depends on size and type of input. Interested in: best-case scenario, worst-case scenario, worst-case scenario.\

To compare algorithms, their relative rate of growth is important.\

<ins>Order of Magnitude O(f(n))</ins>: measures how the number of steps grows with input size (n). For dominant part of the algorithm.\

Let T() be the exact number of steps. T(n), T(5n), T(5n+100), T(4500n+2000) all have approximately the same approximate growth in input size n (they all grow linearly with n)

### Big-O notation (Landau's symbol)

Describes how fast an algorithm grows relative to the input. Describes the amount of time an algorithm needs to run by analyzing asymptotic behavior of functions. e.g. as sample size n goes to infinity.\

<ins>Order of Magnitude O(f(n))</ins>: measures how the number of steps grows with input size (n). For dominant part of the algorithm.\

Let T(n) represent the exact run time (or steps) of an algorithm as a function of number of inputs, n.\

Let O(n) represent the approximate run time (or steps) as a function of number of inputs, n.\

E.g. T(n) = 1 + n^2 + log(n) + n. Then, O(T(n)) = n^2\

```
O(5n)                  = O(n)
O(n^2-n+5)             = O(n^2)
O(2n^3 - 4n + 9)       = O(n^3)
O(n^2log(n) + n^2 + 2) = O(n^2log(n))   
```

ranking
```
O(1)             # constant time              best
O(log n)         # logarithmic time           pretty great
O(n)             # linear time                good
O(n log n)       # log-linear "linearithmic"  descent
O(n^2)           # quadratic time             kind of slow
O(n^3)           # cubic time                 poor performance
O(2^n)           # exponential time           very poor
O(n!)            # factorial time             intolerably slow
```

examples\
O(1)
```python
def isTrue(value):
	return True
```
O(n)
```python
def findNumber(number, list):
	for i in list:
		if i == number:
			return number
```
O(n^2)
```python
n=3
for i in range(n):
	for j in range(n):
		x = i
		y = j
		print("[%s,%s]" % (x,y))
```

If two algorithms have the same time complexity e.g. O(n), but one algorithm has more steps T(n) = 2n versus T(n) = 10n, we say the algorithms have equal time scaling, but one will be faster in practice.\

In other words, when looking at big-O notation we are concerned with relative rate of growth, rather than actual time.\

If-else statements are handled by considering the worst case scenario of the two cases.\

For loops execute n times, where n is the size of the number of loop iterations.\

An algorithm is O(log n) if it takes constant time O(1) to cut the problem size by a fraction. Good example is binary search: technique for searching for an item in a sorted list. The problem size is halved with each iteration. O(log n) efficient for handling large datasets.

If a problem must be solved with an exponential time algorithm, it is typically called <ins>intractible</ins>, meaning it is solvable, but not within practical time limits.

### Timing code

Things to consider:\

Resource allocations: if a computer is running multiple processes in background already, taking up memory, that might have an effect on how fast code runs.\

coffee breaks: i.e. if people have other tasks to do, does the code really need to run in 2 minutes rather than 5 minutes? Consider the practical use cases for the program. Running in 2 minutes versus 5 minutes might not make all the much of a practical difference.\

Costs: e.g. cloud computing environment. Memory might more expensive than computing cycles. you might pay extra for a faster processor, or you might pay extra for greater bandwidth. It could be cheaper to run faster but take more memory, and you could analyze that and determine what the most cost effective computing solution is. You could be doing a tremendous amount of downloading and uploading, and so maybe it makes sense to pay for a slow processor because most of the work is not related to the processor. etc.

You can use the UNIX utility 'time' to time code. "real" time refers to actual clock time elapsed (i.e. looking at the clock before and after). "user" time refers to amount of CPU time spent outside the kernal; might not be relevant based on the type of computing the program is doing. "sys" time refers to the amount of CPU time spent inside the kernel specific functions. Most important is probably the "real" time. user and sys time is helpful for getting information about the application performs on your system. I.e. if your user + sys time is less than real time, then you might have I/O issues (a lot of the time spent in your program is spent reading and writing to files and is not really a problem associated with your program).

```bash
>time python yourprogram.py

real    0m1.028s
user    0m0.001s
sys     0m0.003s
```

examples:

```bash
>time echo "hello world"
hello world

real    0m0.000s
user    0m0.000s
sys     0m0.000s
```

```bash
>time sleep 5


real    0m5.005s
user    0m0.001s
sys     0m0.002s
```

```bash
>more test.py
for i in range(1000):
    print(i)

>time python test.py
1
2
...
999

real    0m0.047s
user    0m0.030s
sys     0m0.012s
```

```time``` module in python standard library helpful. timing the beginning and end of the function is helpful to measure the actual timing of the function, preventing the timing of other computer processes from obfuscating the time it takes for the actual code to run.
```python
# my_script.py
import time

def timed_func():
	start = time.time()
	
	for i in range(10000000):
		total = total + 1000

	end = time.time()
	print("%10.7f s" % (end-start))

timed_function()
```

```bash
>python my_script.py

0.5992429 seconds
```
Each time the function is timed, the time will be different. This is because each time the code run, it is competing for resources with the rest of the processes happening on the computer (the amount of computing resources used by a CPU at any given time transient).

Can implement your own timer:
```python
import time

class Timer:
	def __enter__(self):
		self.start = time.time()
		return self

	def __exit__(self):
		self.end = time.time()
		self.seconds = self.end - self.start
```

```python
# script.py
with Time() as t:
	for i in range(10000):
		x = 10
print(t.seconds)
```

```bash
>python script.py
0.00026...
```

Above technique is very helpful to time code in many different places and not have to write time statements everywhere.

### Data Serialization (Pickle)

```Pickle``` implements binary protocols for serializing and de-serializing pythonobjects. Serialize is a fancy word that means turn objects into data that can be persistent (can save data objects to disks and then later on get them from the disk and bring them back into an application).

Pickling is a process whereby a python object hierarchy is converted into a byte stream. Unpickling is the inverse operation.

serialization: Object --> stream of bytes --> (written to memmory) or (written to file)

deserialization: (data in memmory) or (data in file) --> stream of bytes --> object

serialization in other languages might be called "marshalling", "flattening", or "arching".

example: serialization, writing data to file
```python
import pickle

fav_color = {"lion": "yellow", "kitty":"red"}

with open('color.pickle', 'wb') as f:
	pickle.dump(fav_color,f)
```

Keep in mind, pickled data not inherently safe. Can easily be read by opening the file. In standard library, a warning is issued with the pickle module because it is not secure against erroneously or maliciously constructed data. Never unpickle data received from untrusted or unauthenticated sources.

example: deserialization, reading data from file
```python
import pickle

with open('color.pickle', 'rb') as f:
	fav_color = pickle.laod(f)
```

remember file extensions do not physically mean anything. Saving the file with the extension ".pickle" is simply good etiquette for letting others know it is a pickle file.

JSON vs pickle: JSON has text serialization only. However, JSON is human readable (pickle files not very readable). JSON is not language specific... it is the defacto language standard right now way for sending data around the web (pickle strictly limited to python). However, the advantages of using Pickle are that it allows serialization of custom objects in python, and because the data is stored in binary format, it is in fact faster to read in / send data than by doing so with JSON data (i.e. if you are working with binary data, you are working with less data)

### Higher Order Functions

Python functions are "first-class citizens", meaning they can be passed around by name.

<ins>Higher Order Functions</ins> are functions that operate on other functions: take a function as argument and return a function.

```python
def f(x):
	""""""
	return x*2

g = lambda x: x*2

print(f(2))
print(f(4))
```

```map, reduce, filter``` are helpful higher order functions in python. ```lambda``` is a useful feature as parameters to higher order functions.

Some programming languages exclusively use functional programming paradigm (e.g. Haskell).

Technically, Python's features of mutability and data structures don't allow true functional programming functionality. Python's focus on practicality has led it to assimilate many features of functional programming.

```map()``` is a function that applies a function to all members of a sequence. Returns the result as a map object.

Example

```python
# example procedural style
def squared(x):
	return x**2

numbers = [1,2,3,4,5,6]

squared_nums = []
for i in numbers:
	squared_nums.append(squared(i))

# example functional style

squared_nums = list(map(squared,numbers))
```

```lambda``` operator creates small anonymous (unnamed) functions. Found in many languages (Swift, python, LISP). Core feature of other languages (Haskell, OCaml).

```python
# lambda syntax

result = lambda arglist: expression

# ex
f = lambda x,y: x+y
```

Use of lambda is mostly a matter of style. Makes sense to use lambda when you're going to use a function one time.

Useful for sorting.

```python
people.sort(key=lambda x: x.name)
people.sort(key=lambda x: x.age)
sorted(people, key = lambda x: x.name)
```

```lambda``` also useful in the sense it can be used in higher order function calls. allows us to create functions in-situ as needed:

```python
nums = [1,2,3,4,5,6,7]
nums_squared = map(lambda x: x**2, nums)
```

```filter()``` runs through each element on an iterable object, applies a function to each element, returns only elements of list that evaluate to True.

```python
result = filter(lambda x: x ==True, [True, False, True])
```

```filter()``` runs through each element on an iterable object, applies a function to each element, returns only elements of list that evaluate to True.

```python
def even(x):
	return x % 2 == 0

fib = [1,1,2,3,5,8,13,21,34,55]
result = filter(even, fib)
# [2,8,34]
```

can simplify more:
```python
fib = [1,1,2,3,5,8,13,21,34,55]
result = filter(lambda x: x % 2 == 0, fib)
# [2,8,34]
```

```python
# remove all "0" from a list
nums = [1,4,0,4,5,7,78,20,11,0,2,0]
result = filter(lambda x: x != 0, nums)
# [1,4,4,5,7,78,20,11,2]
```

```reduce()``` continually applies a function to an iterable with the sum to create a cumulative sum of the results, returning a single value. Reduce not in std library. Import from ```functools```.

```python
from functools import reduce
reduce(function,iterable[,initializer])
```

ex:
```python
from functools import reduce
reduce(lambda x,y: x+y,[1,1-2]])
# 0

reduce(lambda x,y: x+y,["c","a","t"]])
# "cat"

nums = [92, 26, 34, 26, 39, 40]
avg = reduce(lambda x,y: x+y, nums) / len(nums)
```

The ```map-reduce-filter``` pattern is a framework for processing huge datasets on distributable problems, which was heart of Google data processing for years. The Hadoop framework is one of the most popular frameworks for map-reduce today.

The map-reduce premise involves taking lots of data at a repository, breaking into chunks, assigning it to multiple processor nodes ('map' step), then in a reduce step has processor nodes reduce the data back together.

FYI, the reduce() function is a bit overkill. Quote from Guido Van Rossum

```
"So now reduce(). This is actually the one I've always hated most, because, apart from a few examples involving + or *, almost every time I see a reduce() call with a non-trivial function argument, I need to grab pen and paper to diagram what's actually being fed into that function before I understand what the reduce() is supposed to do. So in my mind, the applicability of reduce() is pretty much limited to associative operators, and in all other cases it's better to write out the accumulation loop explicitly."
```

List comprehension provide a more readable way to perform higher-order functions.

### List Comprehension

List comprehension is a way to define and create lists in Python:

```python
new_list = [expression for member in iterable]
```

The intent behind the notation of list comprehensions was to mimic well-known notation for sets use by mathmaticians. For example, "x^2 for x in the set of real numbers":

```python
squared_nums = [x**2 for x in nums]
```

Here's an example of how a list comprehension can be more elegant than using higher order functions:
```python
# higher order functions
squares = list(map(lambda x: x*x, list(range(10))))

# list comprehensions
squares = [i*i for i in range(10)]
```

more examples:
```python
def get_price_w_tax(txn):
	return txn * (1 + TAX_RATE)

purchases = [1.09, 23.54, 23.10]
final_prices = [get_price_w_tax(i) for i in purchases]
```

example of cross products:
```python
# cross product of lists
colors = ["red", "green", "yellow", "blue"]
objs = ["house","car","tree"]
colored_objs = [ (x,y) for x in colors for y in objects]
```

list comprehensions very versatile:
```python
nums = [(1,1),(2,2),(3,3),(4,4)]
sums = [x+y for x,y in nums]
```

Can use conditional logic in list comprehensions.
```python
new_list = [expression for member in iterable if condition]
```

ex:
```python
sentence = 'once upon a time in mexico'

vowels = [letter for letter in sentence if letter in 'aeiou']
```

```python
def is_vowel(letter):
	vowels = 'aeious
	return letter in vowel

vowels = [letter for letter in sentence if is_vowel(letter)]
```

Can use if statement statements in the expression within list comprehension:
```python
data = [i if not isinstance(i,str) else 0.0 for i in original_data]
```

Can also use set and dictionary comprehension, but these are not very common:
```python
quote = "something wicked this way comes."
vowels = {i for i in quote if i in 'aeiou'}
# {'a','o','e','i'}
```

```python
# unique cross product of lists
colors = ["red", "green", "yellow", "blue"]
objs = ["house","car","tree"]
colored_objs = { (x,y) for x in colors for y in objects}
```

dictionary comprehension:
```python
squares = {i : i*i for i in range(10)}
```

can use list comprehensions to return a generator:
```python
for i in (x*2 for x in range(10)):
	print(i)
```

List comprehension is simply another tool to help accomplish tasks that may or may not simplify code.

### Iterators and Generators

<ins>Iterators</ins> provide a mechanism to move through a collection. Iterator is any type that can be used in 'for in' loop.

e.g.
```python
for i in range(0,100):
	# stuff
```

```List, tuple, dict, set``` are standard python iterables.

```map(),reduce(),zip()``` are also iterables.

File handles are also iterables:
```python
f = open("myfile.txt")
for line in f.readlines:
	# stuff
```

So, an iterable object is something that we can define what we want returned from a collection of some type. File is an iterator that returns the next line, string returns the next character, list returns the next element.

The behavior of an iterable by implementing the following special python methods: ```__iter__()```, ```__next__()```.

```__iter__()``` is called when the iteration is initialized. example:
```python
def __iter__(self):
	self.x = 0
	return self

def __next__(self):
	# store current value of x
	x = self.x

	# stop iteration if limit is reached
	if x > self.limit:
		raise StopIteration 
		# ^this stops iteration. doesn't throw error. 

	# else increment and return old value
	self.x = x+1
	return x
```

example implementation:
```python
class Counter:
	def __iter__(self):
		self.count = 0
		return self

	def __next__(self):
		self.count += 1
		if self.count > 10:
			raise StopIteration
		return self.count

c = Counter()
for i in c:
	print(i)
```

Some of the built-in python functions like ```list,sum,min,max``` know about iterators:
```python
list(Counter())
sum(Counter())
min(Counter())
max(Counter())
```

<ins>Generators</ins>: are python functions that generate iterators. These can be more powerful and potentially more convenient that iterators.

Generators rely on a function called ```yield```, which returns a generator that runs the code you have written:

```python
def count_from(i):
	while True:
		yield i
		i+=1

numbers = count_from(1)
print(numbers.next()) # 1
print(numbers.next()) # 2
print(numbers.next()) # 3
```

How to make a generator: write a regular function and call yield to produce a value. When another value is needed, the generator function picks up where it left off. Raise the StopIteration exception or call return when you are done.

```python
def big_random_num():
	while True:
		num = random.randint(1,100)
		print(num)
		if num < 10:
			print("less than 10")
			raise StopIteration
		else:
			yield number

for random_num in big_random_num():
	print("number is ... %d!" (random_num))
```

Since python 3.5, ```StopIteration``` has been replaced with solely ```return```, I think. See next section on creating environments (i.e. to be able to run python 3.4 if you had code that used StopIteration, and you needed to be able to run that code).

You can do wonky things with generators
```python
def generate_stuff():
	x=2
	y=3
	yield x,y,x+y
	yield "hi"
	yield "bye"
	return

g = generate_stuff():
print(g.next()) # (2,3,5)
print(g.next()) # Hi
print(g.next()) # Bye
```

### creating environments

By default, with anaconda the ```base``` environment is used. We can setup developments specifically for projects, however.

e.g. setting up python 3.4 environment. name it py34
```bash
>conda create --name py34 python=3.4
```

To activateenvironment:
```bash
>conda activate py34
```

To deactivate environment:
```bash
>conda deactivate py34
```
