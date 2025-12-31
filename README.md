# Python-Programming

# 🐍 Python Basics

## 1. Printing "Hello, World!" in Python

### Syntax
print("Hello, World!")

### Explanation
- print() is a built-in function in Python.
- Text must be written inside quotes (" " or ' ').
- Python is case-sensitive.
- No semicolon is required.

### Output
Hello, World!

--------------------------------------------------

## 2. Inner Working of Python
(Source Code → Bytecode → Python Virtual Machine)

### Execution Flow
Python Source Code (.py)
        ↓
Bytecode (.pyc)
        ↓
Python Virtual Machine (PVM)
        ↓
Output

--------------------------------------------------

### Step 1: Python Source Code
Example:
print("Hello, World!")

File saved as:
hello.py

--------------------------------------------------

### Step 2: Compilation to Bytecode
- Python first compiles the source code.
- Checks syntax and indentation errors.
- Generates bytecode (.pyc).
- Bytecode is platform independent.
- Stored inside __pycache__ folder.

Example:
__pycache__/hello.cpython-312.pyc

--------------------------------------------------

### Step 3: Python Virtual Machine (PVM)
- PVM reads the bytecode.
- Executes bytecode line by line.
- Converts bytecode into machine instructions.
- PVM is software, not hardware.

--------------------------------------------------

### Summary of Inner Working

Source Code → Human-readable Python code
Bytecode    → Intermediate code (.pyc)
PVM         → Executes bytecode line by line

--------------------------------------------------

## 3. Why Python Is an Interpreted Language

### Explanation
- Python code is not directly converted into machine code.
- It is first compiled into bytecode.
- Bytecode is interpreted by Python Virtual Machine (PVM).
- Execution happens line by line.

--------------------------------------------------

### Comparison

C / C++  → Compiled directly to machine code  
Java     → Compiled to bytecode → JVM  
Python   → Compiled to bytecode → Interpreted by PVM  

--------------------------------------------------

### Reasons Python Is Called Interpreted
- No manual compilation step required.
- Line-by-line execution.
- Easy debugging.
- Platform independent.

--------------------------------------------------

## 4. Advantages of Python Execution Model

- Simple and readable syntax
- Platform independent
- Easy debugging
- Automatic memory management
- Faster development

--------------------------------------------------

### Final Summary
Python first compiles source code into bytecode and then interprets it using the Python Virtual Machine, which is why Python is called an interpreted language.

--------------------------------------------------

##  Python Shell

### Definition
Python Shell is an interactive environment where Python code is executed line by line immediately after it is entered.

### How to Open Python Shell
- Open Command Prompt / Terminal
- Type:
  python
- Press Enter

### Prompt Symbol
>>>

### Example
>>> print("Hello Python")
Hello Python

>>> 5 + 3
8

### Features of Python Shell
- Immediate execution
- No need to save files
- Useful for testing and debugging
- Good for beginners

### Difference Between Shell and Script

Python Shell → Interactive, temporary execution  
Python Script → Saved in .py file, reusable

--------------------------------------------------

## 2. Import Statements in Python

### Definition
Import statements are used to include modules so that their functions, classes, and variables can be used in a program.

--------------------------------------------------

### Types of Import Statements

### 1. import module_name
Imports the entire module.

Example:
import math
print(math.sqrt(16))

--------------------------------------------------

### 2. import module_name as alias
Imports module with a short name.

Example:
import math as m
print(m.sqrt(25))

--------------------------------------------------

### 3. from module_name import function_name
Imports specific function from a module.

Example:
from math import sqrt
print(sqrt(36))

--------------------------------------------------

### 4. from module_name import *
Imports all functions and variables (not recommended).

Example:
from math import *
print(sqrt(49))

--------------------------------------------------

### Advantages of Using Import
- Code reusability
- Organized programs
- Saves development time
- Access to built-in libraries

--------------------------------------------------

## 3. Python Modules

### Definition
A module is a file containing Python code (functions, variables, classes) that can be reused in other programs.

### Types of Modules
- Built-in modules
- User-defined modules
- Third-party modules

Examples:
math, os, sys, random

--------------------------------------------------

## 4. OS Module

### Definition
The os module provides functions to interact with the operating system such as file handling, directory management, and environment variables.

--------------------------------------------------

### Commonly Used Functions of OS Module

### 1. os.getcwd()
Returns the current working directory.

Example:
import os
print(os.getcwd())

--------------------------------------------------

### 2. os.listdir(path)
Returns list of files and folders in a directory.

Example:
import os
print(os.listdir())

--------------------------------------------------

### 3. os.mkdir("folder_name")
Creates a new directory.

Example:
import os
os.mkdir("test_folder")

--------------------------------------------------

### 4. os.makedirs("path")
Creates directories recursively.

Example:
import os
os.makedirs("parent/child")

--------------------------------------------------

### 5. os.remove("file_name")
Deletes a file.

Example:
import os
os.remove("data.txt")

--------------------------------------------------

### 6. os.rmdir("folder_name")
Deletes an empty directory.

Example:
import os
os.rmdir("test_folder")

--------------------------------------------------

### 7. os.rename("old_name", "new_name")
Renames a file or directory.

Example:
import os
os.rename("old.txt", "new.txt")

--------------------------------------------------

### 8. os.path.exists(path)
Checks whether a file or directory exists.

Example:
import os
print(os.path.exists("data.txt"))

--------------------------------------------------

### 9. os.path.join(path1, path2)
Joins paths safely.

Example:
import os
print(os.path.join("folder", "file.txt"))

--------------------------------------------------

## 5. Summary

- Python Shell executes code interactively.
- Import statements allow using modules.
- Modules help in code reuse.
- OS module allows interaction with operating system.

--------------------------------------------------

### One Line Summary
Python Shell is used for quick execution, import statements bring modules into programs, and the os module helps Python interact with the operating system.


## 1. Mutable and Immutable Data Types

### Definition
- Mutable data types can be changed after creation.
- Immutable data types cannot be changed after creation.

--------------------------------------------------

## 2. Immutable Data Types in Python

### Definition
Immutable objects do not allow modification of their value after creation. Any change creates a new object in memory.

### List of Immutable Data Types
- int
- float
- complex
- bool
- str
- tuple
- frozenset
- bytes

--------------------------------------------------

### Example (Immutable Behavior)

x = 10
print(id(x))

x = x + 5
print(id(x))

Explanation:
- A new object is created for value 15
- Old object (10) remains unchanged

--------------------------------------------------

### String Example

s = "hello"
s = s + " world"

Explanation:
- Original string "hello" is not modified
- New string "hello world" is created

--------------------------------------------------

## 3. Mutable Data Types in Python

### Definition
Mutable objects allow modification of their content without changing their memory location.

### List of Mutable Data Types
- list
- set
- dict
- bytearray

--------------------------------------------------

### Example (Mutable Behavior)

lst = [1, 2, 3]
print(id(lst))

lst.append(4)
print(id(lst))

Explanation:
- Same object is modified
- Memory location remains same

--------------------------------------------------

## 4. Understanding Referencing in Python (Easy Explanation)

### What is Referencing?
Referencing means variable names point to objects in memory, not to values.

--------------------------------------------------

### Example

a = 10
b = a

Explanation:
- a and b both reference the same object (10)
- No new object is created

--------------------------------------------------

### Check Memory Reference

print(id(a))
print(id(b))

Both ids will be same.

--------------------------------------------------

## 5. Referencing with Immutable Objects

### Example

a = 10
b = a

a = 20

Explanation:
- a now points to a new object (20)
- b still points to old object (10)

--------------------------------------------------

### Diagram Representation

a ──► 20  
b ──► 10  

--------------------------------------------------

## 6. Referencing with Mutable Objects

### Example

lst1 = [1, 2, 3]
lst2 = lst1

lst1.append(4)

Explanation:
- lst1 and lst2 refer to the same list
- Change through one reference affects the other

--------------------------------------------------

### Result

lst1 → [1, 2, 3, 4]  
lst2 → [1, 2, 3, 4]  

--------------------------------------------------

## 7. Copying Mutable Objects

### Shallow Copy

lst1 = [1, 2, 3]
lst2 = lst1.copy()

Explanation:
- New object is created
- Changes in one do not affect the other

--------------------------------------------------

### Deep Copy (Concept)

- Copies object and all nested objects
- Requires copy module
- Used for nested structures

--------------------------------------------------

## 8. Why Python Uses This Model

- Memory efficient
- Faster execution
- Easier object management
- Supports garbage collection

--------------------------------------------------

## 9. Key Differences Summary

Mutable:
- Can change after creation
- Same memory location
- Examples: list, dict, set

Immutable:
- Cannot change after creation
- New object created on change
- Examples: int, str, tuple

--------------------------------------------------

### One Line Summary
In Python, variables reference objects in memory; mutable objects can change in place, while immutable objects create new objects when modified.

--------------------------------------------------

# Object Types / Data Types

- Number : 1234, 3.1415, 3+4j, 0b111, Decimal(), Fraction()
- String : 'spam', "Bob's", b'a\x01c', u'sp\xc4m'
- List : [1, [2, 'three'], 4.5], list(range(10))
- Tuple : (1, 'spam', 4, 'U'), tuple('spam'), namedtuple
- Dictionary : {'food': 'spam', 'taste': 'yum'}, dict(hours=10)

- Set : set('abc'), {'a', 'b', 'c'}

- File : open('eggs.txt'), open(r'C:\ham.bin', 'wb')

- Boolean : True, False
- None : None
- Funtions, modules, classes

- Advance: Decorators, Generators, Iterators, MetaProgramming

--------------------------------------------------

## 1. List

### Definition
A list is an ordered, mutable collection of elements that allows duplicate values.

### Syntax
my_list = [1, 2, 3, 4]

--------------------------------------------------

### Common List Functions

append()   → Adds element at the end  
insert()   → Inserts element at specific index  
remove()   → Removes specified element  
pop()      → Removes element by index  
sort()     → Sorts the list  
reverse()  → Reverses the list  
len()      → Returns number of elements  

--------------------------------------------------

### Implementation Example

numbers = [10, 20, 30]

numbers.append(40)
numbers.insert(1, 15)
numbers.remove(20)
numbers.pop()
numbers.sort()

print(numbers)

--------------------------------------------------

## 2. String

### Definition
A string is an ordered, immutable sequence of characters.

### Syntax
text = "Hello Python"

--------------------------------------------------

### Common String Functions

upper()     → Converts to uppercase  
lower()     → Converts to lowercase  
strip()     → Removes whitespace  
replace()   → Replaces characters  
split()     → Splits string into list  
len()       → Returns length  

--------------------------------------------------

### Implementation Example

text = "  Python Programming  "

print(text.upper())
print(text.strip())
print(text.replace("Python", "Java"))
print(text.split())

--------------------------------------------------

## 3. Tuple

### Definition
A tuple is an ordered, immutable collection of elements.

### Syntax
my_tuple = (1, 2, 3)

--------------------------------------------------

### Common Tuple Functions

count() → Counts occurrences of element  
index() → Returns index of element  
len()   → Returns number of elements  

--------------------------------------------------

### Implementation Example

t = (10, 20, 30, 20)

print(t.count(20))
print(t.index(30))

--------------------------------------------------

## 4. Dictionary

### Definition
A dictionary is an unordered, mutable collection of key-value pairs.

### Syntax
my_dict = {"name": "Aditya", "age": 18}

--------------------------------------------------

### Common Dictionary Functions

keys()    → Returns all keys  
values()  → Returns all values  
items()   → Returns key-value pairs  
get()     → Returns value for key  
update()  → Updates dictionary  
pop()     → Removes key-value pair  

--------------------------------------------------

### Implementation Example

student = {"name": "Aditya", "branch": "CSE"}

student["year"] = 1
student.update({"age": 18})
student.pop("branch")

print(student.keys())
print(student.values())
print(student)

--------------------------------------------------

## 5. Set

### Definition
A set is an unordered, mutable collection of unique elements.

### Syntax
my_set = {1, 2, 3}

--------------------------------------------------

### Common Set Functions

add()        → Adds element  
remove()     → Removes element  
discard()    → Removes element safely  
union()      → Combines sets  
intersection() → Common elements  
difference() → Elements in one set only  

--------------------------------------------------

### Implementation Example

A = {1, 2, 3}
B = {3, 4, 5}

A.add(6)
A.remove(2)

print(A.union(B))
print(A.intersection(B))
print(A.difference(B))

--------------------------------------------------

## 6. Comparison Summary

List        → Ordered, Mutable, Duplicates allowed  
String      → Ordered, Immutable  
Tuple       → Ordered, Immutable  
Dictionary  → Unordered, Mutable, Key-Value pairs  
Set         → Unordered, Mutable, Unique elements  

--------------------------------------------------

### One Line Summary
Python provides different data types like list, string, tuple, dictionary, and set to store and manage data efficiently based on mutability, order, and uniqueness.

# 🐍 Python Numbers & Random Module Notes

--------------------------------------------------

## 1. Numbers in Python

### Definition
Numbers in Python are used to store numeric values and perform mathematical operations.

--------------------------------------------------

## 2. Types of Numbers

### 1. Integer (int)
Whole numbers without decimal points.

Example:
x = 10
y = -5

--------------------------------------------------

### 2. Floating Point (float)
Numbers with decimal points.

Example:
pi = 3.14
temp = -2.5

--------------------------------------------------

### 3. Complex Number (complex)
Numbers with real and imaginary parts.

Syntax:
a + bj

Example:
z = 2 + 3j

--------------------------------------------------

## 3. Type Conversion (Type Casting)

int()    → Converts to integer  
float()  → Converts to float  
complex() → Converts to complex  

Example:
x = int(5.8)
y = float(10)
z = complex(2)

--------------------------------------------------

## 4. Arithmetic Operations on Numbers

Addition        → +  
Subtraction     → -  
Multiplication  → *  
Division        → /  
Floor Division  → //  
Modulus         → %  
Exponentiation  → **  

Example:
a = 10
b = 3

print(a + b)
print(a // b)
print(a ** b)

--------------------------------------------------

## 5. Random Module

### Definition
The random module is used to generate random numbers and perform random operations.

--------------------------------------------------

### Import Random Module

import random

--------------------------------------------------

## 6. Common Random Functions

### 1. random.random()
Returns a random float between 0.0 and 1.0.

Example:
import random
print(random.random())

--------------------------------------------------

### 2. random.randint(start, end)
Returns a random integer between start and end (inclusive).

Example:
import random
print(random.randint(1, 10))

--------------------------------------------------

### 3. random.choice(sequence)
Returns a random element from a sequence.

Example:
import random
colors = ["red", "blue", "green"]
print(random.choice(colors))

--------------------------------------------------

### 4. random.shuffle(sequence)
Shuffles the sequence randomly (modifies original).

Example:
import random
nums = [1, 2, 3, 4, 5]
random.shuffle(nums)
print(nums)

--------------------------------------------------

### 5. random.uniform(start, end)
Returns a random float between start and end.

Example:
import random
print(random.uniform(1.5, 5.5))

--------------------------------------------------

## 7. Operator Precedence in Python

### Definition
Operator precedence determines the order in which operations are evaluated in an expression.

--------------------------------------------------

### Precedence Order (High → Low)

()          → Parentheses  
**          → Exponentiation  
+, -        → Unary plus, minus  
*, /, //, % → Multiplication, Division  
+, -        → Addition, Subtraction  
==, !=, >,< → Comparison  
and         → Logical AND  
or          → Logical OR  

--------------------------------------------------

### Example

result = 10 + 2 * 3 ** 2
print(result)

Evaluation:
3 ** 2 = 9  
2 * 9 = 18  
10 + 18 = 28  

--------------------------------------------------

## 8. Math Functions with Numbers

abs()   → Absolute value  
round() → Rounds number  
pow()   → Power function  
max()   → Maximum value  
min()   → Minimum value  

Example:
print(abs(-10))
print(round(3.6))
print(pow(2, 3))

--------------------------------------------------

## 9. Summary

- Python supports int, float, and complex numbers.
- Random module generates random values.
- randint(), choice(), shuffle() are commonly used.
- Operator precedence controls expression evaluation.

--------------------------------------------------

### One Line Summary
Python provides powerful numeric data types and random utilities, with well-defined operator precedence for accurate mathematical computations.


--------------------------------------------------

## 1. Strings in Python

### Definition
A string is an ordered, immutable sequence of characters enclosed in single or double quotes.

### Syntax
s1 = "Python"
s2 = 'Programming'

--------------------------------------------------

## 2. Common String Methods

upper()     → Converts string to uppercase  
lower()     → Converts string to lowercase  
title()     → Converts to title case  
capitalize() → Capitalizes first character  
strip()     → Removes leading and trailing spaces  
lstrip()    → Removes leading spaces  
rstrip()    → Removes trailing spaces  
replace()   → Replaces substring  
find()      → Returns index of substring  
count()     → Counts occurrence of substring  
startswith() → Checks starting characters  
endswith()  → Checks ending characters  
len()       → Returns length of string  

--------------------------------------------------

### Implementation Example (String Methods)

text = "  python programming  "

print(text.upper())
print(text.strip())
print(text.replace("python", "java"))
print(text.count("m"))

--------------------------------------------------

## 3. Converting List to String

### Method 1: Using join()

### Definition
join() joins list elements into a string using a separator.

### Syntax
separator.join(list)

--------------------------------------------------

### Example

words = ["Python", "is", "awesome"]

sentence = " ".join(words)
print(sentence)

--------------------------------------------------

### Method 2: Using loop (basic)

result = ""
for word in words:
    result += word + " "

print(result.strip())

--------------------------------------------------

## 4. Converting String to List

### Method 1: Using split()

### Definition
split() converts a string into a list by separating elements.

--------------------------------------------------

### Example

text = "Python is easy"
words = text.split()
print(words)

--------------------------------------------------

### Method 2: Split by specific character

data = "apple,banana,orange"
fruits = data.split(",")
print(fruits)

--------------------------------------------------

## 5. String Indexing

### Definition
Indexing is used to access individual characters in a string.

--------------------------------------------------

### Example

s = "Python"

s[0]   → P  
s[1]   → y  
s[-1]  → n  

--------------------------------------------------

## 6. String Slicing

### Definition
Slicing is used to extract a portion of a string.

### Syntax
string[start : end]

--------------------------------------------------

### Examples

s = "Programming"

print(s[0:6])
print(s[3:])
print(s[:7])
print(s[-4:])

--------------------------------------------------

## 7. String Slicing with Skipping (Step)

### Syntax
string[start : end : step]

--------------------------------------------------

### Examples

s = "Programming"

print(s[::1])     → Normal  
print(s[::2])     → Skip every second character  
print(s[1::2])    → Skip from index 1  
print(s[::-1])    → Reverse string  

--------------------------------------------------

## 8. Important Notes

- Strings are immutable.
- Any modification creates a new string.
- IndexError occurs if index is out of range.
- join() works only with string elements.

--------------------------------------------------

## 9. Summary

- Strings store text data.
- String methods manipulate text.
- join() converts list to string.
- split() converts string to list.
- Slicing extracts parts of strings.
- Step allows skipping characters.

--------------------------------------------------

### One Line Summary
Python strings are immutable sequences with powerful methods, easy list conversion, and flexible slicing with skipping support.

--------------------------------------------------

## 1. List in Python

### Definition
A list is an ordered, mutable collection of elements that can store multiple data types and allows duplicate values.

### Syntax
my_list = [1, 2, 3, "Python", True]

--------------------------------------------------

## 2. Properties of List

- Ordered collection
- Mutable (can be changed)
- Allows duplicate elements
- Can store mixed data types
- Indexed (positive & negative)

--------------------------------------------------

## 3. Creating Lists

### Empty List
lst = []

### Using list()
lst = list()

### List with Values
numbers = [10, 20, 30]

--------------------------------------------------

## 4. List Indexing and Slicing

### Indexing
lst = [10, 20, 30, 40]

lst[0]   → 10  
lst[-1]  → 40  

--------------------------------------------------

### Slicing
lst[start : end : step]

Example:
print(lst[1:4])
print(lst[::2])
print(lst[::-1])

--------------------------------------------------

## 5. Common List Methods

append()    → Adds element at end  
extend()    → Adds multiple elements  
insert()    → Inserts at specific index  
remove()    → Removes first occurrence  
pop()       → Removes element by index  
clear()     → Removes all elements  
index()     → Returns index of element  
count()     → Counts occurrences  
sort()      → Sorts list  
reverse()   → Reverses list  
copy()      → Returns shallow copy  

--------------------------------------------------

## 6. List Methods – Implementation

lst = [10, 20, 30]

lst.append(40)
lst.insert(1, 15)
lst.extend([50, 60])
lst.remove(20)
lst.pop()
lst.sort()
lst.reverse()

print(lst)

--------------------------------------------------

## 7. List Usage & Context in Memory

### Memory Behavior
- Lists are mutable objects.
- Stored in heap memory.
- Variables store references to lists, not values.

--------------------------------------------------

### Example (Reference Behavior)

lst1 = [1, 2, 3]
lst2 = lst1

lst1.append(4)

print(lst1)
print(lst2)

Explanation:
- lst1 and lst2 point to the same list.
- Change through one reference affects the other.

--------------------------------------------------

### Copying Lists

### Shallow Copy
lst2 = lst1.copy()

### Using list()
lst2 = list(lst1)

--------------------------------------------------

## 8. Why Lists Are Memory Efficient

- Dynamic resizing
- Stores references to objects
- Faster append operations
- Efficient iteration

--------------------------------------------------

## 9. List Comprehension

### Definition
List comprehension is a concise way to create lists using a single line of code.

--------------------------------------------------

### Syntax
[expression for item in iterable]

--------------------------------------------------

### Example

squares = [x*x for x in range(1, 6)]
print(squares)

--------------------------------------------------

### List Comprehension with Condition

### Syntax
[expression for item in iterable if condition]

--------------------------------------------------

### Example

even_numbers = [x for x in range(1, 11) if x % 2 == 0]
print(even_numbers)

--------------------------------------------------

## 10. Nested List Comprehension

matrix = [[1, 2], [3, 4], [5, 6]]

flatten = [num for row in matrix for num in row]
print(flatten)

--------------------------------------------------

## 11. List vs Tuple (Quick View)

List  → Mutable, uses more memory  
Tuple → Immutable, faster, less memory  

--------------------------------------------------

## 12. Summary

- Lists are ordered and mutable.
- Support many built-in methods.
- Use references in memory.
- List comprehension provides clean and fast list creation.

--------------------------------------------------

### One Line Summary
Python lists are flexible, mutable collections with powerful methods, reference-based memory behavior, and elegant creation using list comprehensions.

# 🐍 Python Dictionary 

--------------------------------------------------

## 1. Dictionary in Python

### Definition
A dictionary is an unordered, mutable collection of key-value pairs where each key is unique.

### Syntax
my_dict = {"name": "Aditya", "age": 18}

--------------------------------------------------

## 2. Dictionary Keys and Values

### Keys
- Must be unique
- Immutable types (int, str, tuple)
- Used to access values

### Values
- Can be any data type
- Can be duplicated

--------------------------------------------------

### Accessing Keys and Values

student = {"name": "Aditya", "branch": "CSE", "year": 1}

print(student.keys())
print(student.values())
print(student.items())

--------------------------------------------------

## 3. Adding and Updating Dictionary Elements

### Adding New Key-Value Pair
student["college"] = "ABC University"

### Updating Existing Value
student["year"] = 2

--------------------------------------------------

## 4. Dictionary Inside Dictionary (Nested Dictionary)

### Definition
A dictionary that contains another dictionary as its value.

--------------------------------------------------

### Example

student = {
    "name": "Aditya",
    "marks": {
        "math": 85,
        "physics": 90,
        "cs": 95
    },
    "year": 1
}

--------------------------------------------------

### Accessing Nested Dictionary Values

print(student["marks"]["math"])
print(student["marks"]["cs"])

--------------------------------------------------

## 5. get() Method in Dictionary

### Definition
get() is used to safely retrieve the value of a key without causing an error if the key does not exist.

--------------------------------------------------

### Syntax
dictionary.get(key, default_value)

--------------------------------------------------

### Example

student = {"name": "Aditya", "age": 18}

print(student.get("age"))
print(student.get("marks"))
print(student.get("marks", 0))

--------------------------------------------------

### Advantage of get()
- Prevents KeyError
- Allows default return value

--------------------------------------------------

## 6. Setting Default Values in Dictionary

--------------------------------------------------

### Method 1: Using setdefault()

### Definition
setdefault() returns the value of a key if it exists; otherwise, it inserts the key with a default value.

--------------------------------------------------

### Syntax
dictionary.setdefault(key, default_value)

--------------------------------------------------

### Example

student = {"name": "Aditya"}

student.setdefault("age", 18)
student.setdefault("name", "Unknown")

print(student)

--------------------------------------------------

### Method 2: Using get() with assignment

Example:

if student.get("branch") is None:
    student["branch"] = "CSE"

--------------------------------------------------

### Method 3: Using collections.defaultdict (Concept)

- Automatically sets default value
- Requires collections module
- Useful for counting problems

--------------------------------------------------

## 7. Removing Dictionary Elements

pop()     → Removes key-value pair  
popitem() → Removes last inserted item  
clear()   → Removes all items  

--------------------------------------------------

### Example

student.pop("year")
student.clear()

--------------------------------------------------

## 8. Dictionary Memory Behavior

- Dictionaries store data as key-value pairs
- Keys are hashed for fast lookup
- Values are accessed using key references
- Lookup time is O(1) on average

--------------------------------------------------

## 9. Summary

- Dictionaries store data in key-value format
- Keys must be unique and immutable
- Nested dictionaries store structured data
- get() avoids KeyError
- setdefault() sets default values safely

--------------------------------------------------

### One Line Summary
Python dictionaries efficiently store key-value data, support nesting, safe access using get(), and easy default value handling using setdefault().


--------------------------------------------------

## 1. Tuple in Python

### Definition
A tuple is an ordered, immutable collection of elements that allows duplicate values.

### Syntax
my_tuple = (1, 2, 3)

--------------------------------------------------

## 2. Properties of Tuple

- Ordered collection
- Immutable (cannot be changed)
- Allows duplicate elements
- Can store mixed data types
- Faster than lists
- Uses less memory

--------------------------------------------------

## 3. Creating Tuples

### Empty Tuple
t = ()

### Single Element Tuple
t = (10,)

### Tuple without Parentheses
t = 10, 20, 30

--------------------------------------------------

## 4. Tuple Indexing and Slicing

### Indexing
t = (10, 20, 30, 40)

t[0]   → 10  
t[-1]  → 40  

--------------------------------------------------

### Slicing
t[start : end : step]

Example:
print(t[1:3])
print(t[::2])
print(t[::-1])

--------------------------------------------------

## 5. Tuple Methods

count() → Returns number of occurrences of an element  
index() → Returns index of an element  

--------------------------------------------------

### Tuple Methods – Implementation

t = (10, 20, 30, 20, 40)

print(t.count(20))
print(t.index(30))

--------------------------------------------------

## 6. Tuple Packing and Unpacking

### Packing
t = 10, 20, 30

--------------------------------------------------

### Unpacking
a, b, c = t

print(a)
print(b)
print(c)

--------------------------------------------------

## 7. Tuple with Loop

t = ("Python", "Java", "C")

for item in t:
    print(item)

--------------------------------------------------

## 8. Tuple in Memory Context

- Tuples are immutable
- Stored in heap memory
- Variables store references
- Cannot change elements after creation

--------------------------------------------------

### Example (Immutability)

t = (1, 2, 3)
t[0] = 10   → Error

--------------------------------------------------

## 9. Why Use Tuples?

- Data safety (cannot be modified)
- Faster iteration
- Used as dictionary keys
- Used for returning multiple values

--------------------------------------------------

## 10. Tuple vs List

Tuple → Immutable, Faster, Less memory  
List  → Mutable, Slower, More memory  

--------------------------------------------------

## 11. Summary

- Tuples are ordered and immutable.
- Support indexing and slicing.
- Have limited methods.
- Efficient for fixed data.

--------------------------------------------------

### One Line Summary
Python tuples are immutable, ordered collections used for fixed data, faster execution, and safe storage.
