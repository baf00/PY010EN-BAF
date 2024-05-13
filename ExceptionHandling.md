enclose code with Try Except statements to handle exceptions

try:
    getfile=open("myfile","r")
    getfile.write("My file for exception handling.")
except:
    print("Unable to open or read the data in the file.")
else:
    print("The file was written successfully.")
finally:
    getfile.close()
    print("File is now closed.")


    Objectives
Understanding Exceptions
Distinguishing Errors from Exceptions
Familiarity with Common Python Exceptions
Managing Exceptions Effectively

Common Exceptions in Python

ZeroDivisionError: This error arises when an attempt is made to divide a number by zero. Division by zero is undefined in mathematics, causing an arithmetic error. For instance:
For example:

result = 10 / 0 
print(result)
# Raises ZeroDivisionError

