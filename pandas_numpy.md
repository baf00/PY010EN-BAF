This module explains the basics of working with data in Python and begins the path with learning how to read and write files. 
Continue the module and uncover the best Python libraries that will aid in data manipulation and mathematical operations.

Learning Objectives
In this module you will learn about:
- Explain how Pandas use data frames.
- Use Pandas library for data analysis.
- Read text files using Python libraries including "open" and "with".
- Utilize NumPy to create one-dimensional and two-dimensional arrays.
- Write and save files in Python.

Download Data
Reading Text Files
A Better Way to Open a File


## Uncomment these if working locally, else let the following code cell run.

# import urllib.request
# url = 'https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0101EN-SkillsNetwork/labs/Module%204/data/example1.txt'
# filename = 'Example1.txt'
# urllib.request.urlretrieve(url, filename)

## Download Example file
# !wget -O /resources/data/Example1.txt https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0101EN-SkillsNetwork/labs/Module%204/data/example1.txt


from pyodide.http import pyfetch

import pandas as pd

filename = "https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0101EN-SkillsNetwork/labs/Module%204/data/example1.txt"

async def download(url, filename):

    response = await pyfetch(url)

    if response.status == 200:

        with open(filename, "wb") as f:

            f.write(await response.bytes())

await download(filename, "example1.txt")

print("done")


Reading Text Files¶

One way to read or write a file in Python is to use the built-in open function. 
The open function provides a File object that contains the methods and attributes you need in order to read, save, and manipulate the file. 
In this notebook, we will only cover .txt files. The first parameter you need is the file path and the file name. An example is shown as follow:

file = open("/resources/data/Example1.txt","r")

The mode argument is optional and the default value is r. In this notebook we only cover two modes:

**r**: Read mode for reading files
**w**: Write mode for writing files

For the next example, we will use the text file Example1.txt. The file is shown as follows:

This is line 1
This is line 2
This is line 3

from a cmd line session:

Last login: Mon Jun  3 07:05:40 on console
bruce@bruce ~ %
bruce@bruce ~ %
bruce@bruce ~ %
bruce@bruce ~ %  vi example1.txt
bruce@bruce ~ % python3
Python 3.8.5 (default, Jul 21 2020, 10:42:08)
[Clang 11.0.0 (clang-1100.0.33.17)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> example1 = "example1.txt"
>>> file1 = open(example1, "r")
>>> file1.name
'example1.txt'
>>> file1.mode
'r'
>>> FileContent = file1.read()
>>> FileContent
'This is line 1\nThis is line 2\nThis is line 3\n\n'
>>> print(FileContent)
This is line 1
This is line 2
This is line 3


>>> type(FileContent)
<class 'str'>
>>> file1.close()
>>>

A Better Way to Open a File

Using the with statement is better practice, it automatically closes the file even if the code encounters an exception. 
The code will run everything in the indent block then close the file object.

# Open file using with

with open(example1, "r") as file1:
    FileContent = file1.read()
    print(FileContent)



>>>
>>> with open(example1, "r") as file1:
...     FileContent = file1.read()
...     print(FileContent)
...
This is line 1
This is line 2
This is line 3


>>> file1.closed
True



>>> print(FileContent)
This is line 1
This is line 2
This is line 3


We don’t have to read the entire file, for example, we can read the first 4 characters by entering three as a parameter to the method **.read()**:

>>> with open(example1, "r") as file1:
...     print(file1.read(4))
...
This


# Read certain amount of characters

with open(example1, "r") as file1:
    print(file1.read(4))
    print(file1.read(4))
    print(file1.read(7))
    print(file1.read(15))





>>>
>>> with open(example1, "r") as file1:
...     print(file1.read(4))
...     print(file1.read(4))
...     print(file1.read(7))
...     print(file1.read(15))
...
This
 is
line 1

This is line 2




# Read certain amount of characters

with open(example1, "r") as file1:
    print(file1.read(16))
    print(file1.read(5))
    print(file1.read(9))



>>> with open(example1, "r") as file1:
...     print(file1.read(16))
...     print(file1.read(5))
...     print(file1.read(9))
...
This is line 1
T
his i
s line 2

>>>

We can also read one line of the file at a time using the method readline
    
# Read one line

with open(example1, "r") as file1:
    print("first line: " + file1.readline())


>>> # Read one line
>>>
>>> with open(example1, "r") as file1:
...     print("first line: " + file1.readline())
...
first line: This is line 1


We can also pass an argument to  readline()  to specify the number of charecters we want to read. However, unlike  read(),  readline() can only read one line at most.

with open(example1, "r") as file1:
    print(file1.readline(20)) # does not read past the end of line
    print(file1.read(20)) # Returns the next 20 chars



>>>
>>>
>>> with open(example1, "r") as file1:
...     print(file1.readline(20)) # does not read past the end of line
...     print(file1.read(20)) # Returns the next 20 chars
...
This is line 1

This is line 2
This


We can use a loop to iterate through each line:

# Iterate through the lines

with open(example1,"r") as file1:
        i = 0;
        for line in file1:
            print("Iteration", str(i), ": ", line)
            i = i + 1


>>>
>>> # Iterate through the lines
>>>
>>> with open(example1,"r") as file1:
...         i = 0;
...         for line in file1:
...             print("Iteration", str(i), ": ", line)
...             i = i + 1
...
Iteration 0 :  This is line 1

Iteration 1 :  This is line 2

Iteration 2 :  This is line 3

Iteration 3 :


We can use the method readlines() to save the text file to a list:

# Read all lines and save as a list

with open(example1, "r") as file1:
    FileasList = file1.readlines()
--------------


Write and Save Files in Python¶
Estimated time needed: 25 minutes

Objectives
After completing this lab you will be able to:

Write to files using Python libraries


Table of Contents¶
Writing Files
Appending Files
Additional File modes
Copy a File


Writing Files¶
We can open a file object using the method write() to save the text file to a list. To write to a file, the mode argument must be set to w. 
Let’s write a file Example2.txt with the line: “This is line A”

# Write line to file
exmp2 = 'Example2.txt'
with open(exmp2, 'w') as writefile:
    writefile.write("This is line A")



 We can read the file to see if it worked:


# Read file

with open(exmp2, 'r') as testwritefile:
    print(testwritefile.read())




>>> with open(example1, "r") as file1:
...     FileasList = file1.readlines()
...
>>>
>>> FileasList[0]
'This is line 1\n'
>>> FileasList[2]
'This is line 3\n'
>>>
>>> # Write line to file
>>> exmp2 = 'Example2.txt'
>>> with open(exmp2, 'w') as writefile:
...     writefile.write("This is line A")
...
14
>>> # Read file
>>>
>>> with open(exmp2, 'r') as testwritefile:
...     print(testwritefile.read())
...
This is line A
>>>
>>> # Write lines to file
>>>
>>> with open(exmp2, 'w') as writefile:
...     writefile.write("This is line A\n")
...     writefile.write("This is line B\n")
...
15
15
>>> #The method .write() works similar to the method .readline(), except instead of reading a new line it writes a new line.
>>> The process is illustrated in the figure. The different colour coding of the grid represents a new line added to the file after each method call.



>>> # Check whether write to file
>>>
>>> with open(exmp2, 'r') as testwritefile:
...     print(testwritefile.read())
...
This is line A
This is line B


 We write a list to a **.txt** file  as follows:


# Sample list of text

Lines = ["This is line A\n", "This is line B\n", "This is line C\n"]
Lines


>>> # Sample list of text
>>>
>>> Lines = ["This is line A\n", "This is line B\n", "This is line C\n"]
>>> Lines
['This is line A\n', 'This is line B\n', 'This is line C\n']
>>>



>>>
>>> # Write the strings in the list to text file
>>>
>>> with open('Example2.txt', 'w') as writefile:
...     for line in Lines:
...         print(line)
...         writefile.write(line)
...
This is line A

15
This is line B

15
This is line C

15




>>> # Verify if writing to file is successfully executed
>>>
>>> with open('Example2.txt', 'r') as testwritefile:
...     print(testwritefile.read())
...
This is line A
This is line B
This is line C



However, note that setting the mode to __w__ overwrites all the existing data in the file.

with open('Example2.txt', 'w') as writefile:
    writefile.write("Overwrite\n")
with open('Example2.txt', 'r') as testwritefile:
    print(testwritefile.read())



>>>
>>>
>>> with open('Example2.txt', 'w') as writefile:
...     writefile.write("Overwrite\n")
...
10
>>>
>>> with open('Example2.txt', 'r') as testwritefile:
...     print(testwritefile.read())
...
Overwrite



Appending Files

 We can write to files without losing any of the existing data as follows by setting the mode argument to append: **a**.  you can append a new line as follows:



# Write a new line to text file

with open('Example2.txt', 'a') as testwritefile:
    testwritefile.write("This is line C\n")
    testwritefile.write("This is line D\n")
    testwritefile.write("This is line E\n")


     You can verify the file has changed by running the following cell:



# Verify if the new line is in the text file

with open('Example2.txt', 'r') as testwritefile:
    print(testwritefile.read())





>>> # Verify if the new line is in the text file
>>>
>>> with open('Example2.txt', 'r') as testwritefile:
...     print(testwritefile.read())
...
Overwrite
This is line C
This is line D
This is line E



Additional modes


It's fairly ineffecient to open the file in a or w and then reopening it in r to read any lines. Luckily we can access the file in the following modes:

r+ : Reading and writing. Cannot truncate the file.
w+ : Writing and reading. Truncates the file.
a+ : Appending and Reading. Creates a new file, if none exists. You dont have to dwell on the specifics of each mode for this lab.



Let's try out the a+ mode:


with open('Example2.txt', 'a+') as testwritefile:
    testwritefile.write("This is line E\n")
    print(testwritefile.read())

There were no errors but read() also did not output anything. This is because of our location in the file.

Most of the file methods we've looked at work in a certain location in the file. .write()  writes at a certain location in the file. .read() reads at a certain location in the file and so on. 
You can think of this as moving your pointer around in the notepad to make changes at specific location.
    
Opening the file in w is akin to opening the .txt file, moving your cursor to the beginning of the text file, writing new text and deleting everything that follows. Whereas opening the file in a is similiar to opening the .txt file, moving your cursor to the very end and then adding the new pieces of text.
It is often very useful to know where the 'cursor' is in a file and be able to control it. The following methods allow us to do precisely this -


.tell() - returns the current position in bytes
.seek(offset,from) - changes the position by 'offset' bytes with respect to 'from'. 
From can take the value of 0,1,2 corresponding to beginning, relative to current position and end

Now lets revisit **a+**

>>>
>>> with open('Example2.txt', 'a+') as testwritefile:
...     print("Initial Location: {}".format(testwritefile.tell()))
...
...     data = testwritefile.read()
...     if (not data):  #empty strings return false in python
...             print('Read nothing')
...     else:
...             print(testwritefile.read())
...
...     testwritefile.seek(0,0) # move 0 bytes from beginning.
...
...     print("\nNew Location : {}".format(testwritefile.tell()))
...     data = testwritefile.read()
...     if (not data):
...             print('Read nothing')
...     else:
...             print(data)
...
...     print("Location after read: {}".format(testwritefile.tell()) )
...
Initial Location: 70
Read nothing
0

New Location : 0
Overwrite
This is line C
This is line D
This is line E
This is line E

Location after read: 70

Finally, a note on the difference between w+ and r+. Both of these modes allow access to read and write methods, however, opening a file in w+ overwrites it and deletes all pre-existing data.
To work with a file on existing data, use r+ and a+. While using r+, it can be useful to add a .truncate() method at the end of your data. This will reduce the file to your data and delete everything that follows.
In the following code block, Run the code as it is first and then run it with the .truncate().



>>>
>>> with open('Example2.txt', 'r+') as testwritefile:
...     data = testwritefile.readlines()
...     testwritefile.seek(0,0) #write at beginning of file
...
...     testwritefile.write("Line 1" + "\n")
...     testwritefile.write("Line 2" + "\n")
...     testwritefile.write("Line 3" + "\n")
...     testwritefile.write("finished\n")
...     #Uncomment the line below
...     #testwritefile.truncate()
...     testwritefile.seek(0,0)
...     print(testwritefile.read())
...
0
7
7
7
9
0
Line 1
Line 2
Line 3
finished
is line D
This is line E
This is line E






    
