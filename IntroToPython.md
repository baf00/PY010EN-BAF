Welcome to “Introduction to Python”.
After watching this video, you will be able to
identify the users of Python.

List the benefits of using Python.

Describe the diversity and inclusion efforts of the Python community.

Python is a powerhouse of a language.

It is the most widely used and most popular


Strings:
using regex
s1 = "Michael Jackson is the best"
pattern = r"Jackson"
if the pattern was r"\W" #Matches any non-word character like , ! and space
result - re.search(patter,s1)

matches = re.findall(pattern,text) 

print every second character with stride
print(e[::2])

print the first 3 elements
print(d[0:3])

txt = "Hello my friends"
x = txt.upper()
print(x)

txt = "Hello my FRIENDS"
x = txt.lower()
print(x)

string.find(substring, start, end)

my_string = "Where's Waldo?"
my_string.find("Waldo")

txt = "I like bananas"
x = txt.replace("bananas", "apples")
print(x)

txt = "welcome to the jungle"
x = txt.split()
print(x)

import re
txt = "The rain in Spain"
x = re.search("^The.*Spain$", txt)

result = re.search("\d\d\d\d", s3)

s3 = "House number - 1105"
if result:
    print("digit found")
else 
    print("digit not found") 

Sub() funtion
new_string = re.sub(pattern, replacement, s3, flags=re.IGNORECASE)
the re.IGNORECASE is optional

result = re.findall(r"as", s2)
print(result)

Congratulations! You have completed this module. At this point, you know that: 

Python can distinguish among data types such as integers, floats, strings, and Booleans.
Integers are whole numbers that can be positive or negative.
Floats include integers as well as decimal numbers between the integers.
You can convert integers to floats using typecasting, but you cannot convert a float to an integer.
You can convert integers and floats to strings.
You can convert an integer or float value to True (1) or False (0).
Expressions in Python are a combination of values and operations used to produce a single result.
Expressions perform mathematical operations such as addition, subtraction, multiplication, and so on.
We use"//" to round off integer divisions, resulting in float values.
Python follows the order of operations (BODMASS) to perform operations with multiple expressions.
Variables store and manipulate data, allowing you to access and modify values throughout your code.
The assignment operator "=" assigns a value to a variable.
":" denotes the value of the variable within the code.
Assigning another value to the same variable overrides the previous value of that variable.
You can perform mathematical operations on variables using the same or different variables.
While performing operations with various variables, modifying a value in one variable will lead to changes in the other variables.
Python string operations involve manipulating text data using tasks such as indexing, concatenation, slicing, and formatting.
A string is usually written within double quotes or single quotes, including letters, white space, digits, or special characters.
A string attaches to another variable and is an ordered sequence of characters.
Characters in a string identify their index numbers, which can be positive or negative.
We use strings as a sequence to perform sequence operations. 
You can input a stride value to perform slicing while operating on a string.
Operations like finding the length of the string, combining, concatenating, and replicating, result in a new string.
You cannot modify an existing string; they are immutable. 
You can perform escape sequences using " " to change the layout of the string.
In Python, you perform tasks such as searching, modifying, and formatting text data with its pre-built String Methods functions.
You apply a method to a string to change its value, resulting in another string. 
You can perform actions such as changing the case of characters in a string, replacing items in a string, finding items in a string, and so on using pre-builtString methods.
