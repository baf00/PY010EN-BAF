Learning Objectives
In this module you will learn about:
Classify conditions and branching by identifying structured scenarios with outputs.
Work with objects and classes.
Explain objects and classes by identifying data types and creating a class.
Use exception handling in Python.
Explain what functions do.
Build a function using inputs and outputs.
Explain how for loops and while loops work.
Work with condition statements in Python, including operators and branching.
Create and use loop statements in Python.


comparisons produce a boolean with if else
if (age>19):  #condition
    print("you will enter")
else:
    print("go see Meat Loaf")
print"move on")

 comparisons produce a boolean with if elif
if (age>19):  #condition
    print("you will enter")
elif(age==18):
    print("go see Pink Floyd")
else:
    print("go see Meat Loaf")
print"move on")

Logic Operators
NOT
OR
if(album_year < 1980)or(album_year)>1989):
    print)"The album was made in the 70s or 90s")
else:
    print("The album was made in the 1980s")
AND


Condition Statements
  Comparison Operators
  Branching
  Logical operators
Quiz on Condition Statement

operators:

equal: ==
not equal: !=
greater than: >
less than: <
greater than or equal to: >=
less than or equal to: <=

Char.	ASCII	Char.	ASCII	Char.	ASCII	Char.	ASCII
A	65	N	78	a	97	n	110
B	66	O	79	b	98	o	111
C	67	P	80	c	99	p	112
D	68	Q	81	d	100	q	113
E	69	R	82	e	101	r	114
F	70	S	83	f	102	s	115
G	71	T	84	g	103	t	116
H	72	U	85	h	104	u	117
I	73	V	86	i	105	v	118
J	74	W	87	j	106	w	119
K	75	X	88	k	107	x	120
L	76	Y	89	l	108	y	121
M	77	Z	90	m	109	z	122


ascii lettters are compared by their nummeric value.
When there are multiple letters, the first letter takes precedence in ordering:
Note: Upper Case Letters have different ASCII code than Lower Case Letters, which means the comparison between the letters in Python is case-sensitive.

Annie = 1996
Jane = 1999
if((Annie % 4) == 0):
    print("Annie was born in a leap year.")
else:
    print("Annie was not born in a leap year.")
if((Jane % 4) == 0):
    print("Annie was born in a leap year.")
else:
    print("Annie was not born in a leap year.")

Annie=1996
Jane=1999
if Annie%4==0:
    print("Annie was born in a leap year")
elif Jane%4==0:
    print("Jane was born in a leap year")
else:
    print("None of them were born in a leap year")

age = 24
if(age<9):
    print("Give them milk porridge.")
elif(age<=14):
    print("Give them a sandwich.")
else:
    print("Give them a burger.")


user_choice = "Withdraw Cash"
if user_choice == "Withdraw Cash":
    amount = input("Enter the amount to withdraw: ")
    if amount % 10 == 0:
        dispense_cash(amount)
    else:
        print("Please enter a multiple of 10.")
else:
    print("Thank you for using the ATM.")


1=2
  SyntaxError:can't assign to literal




Loops
range(3)  is equivalent to  range(0,3)


Range 
Range(10,15)
   [10,11,12,13,14]

Range(N)
    [0,..,N-1]

pseudocode
For square 0 in squares, square 0 = white square

Python
squares=["red","yellow","green","purple","blue"]
for i in range(0,5):
    squares[i]="whtie"

in Python we don't need the iterator variable

squares=["red","yellow","green","purple","blue"]
for square in squares:
    sqiare     #print the square color

squares=["red","yellow","green","purple","blue"]

for i,square in enumerate(squares):
    print(i, square)


How Does Enumerate() Work? Enumerate() is a built-in function of Python. 

This function allows us to loop over something and have an automatic counter. 
And this function works by adding a counter to an iterable and returning it in the form of an enumerate object.


While - only runs if a condition is met

while(squares[i] =='orange'):

count = 1
while count <= 5:
    print(count)
    count += 1

1
2
3
4
5


# While Loop Example

dates = [1982, 1980, 1973, 2000]

i = 0
year = dates[0]

while(year != 1973):    
    print(year)
    i = i + 1
    year = dates[i]
    

print("It took ", i ,"repetitions to get out of loop.")


PlayListRatings = [10, 9.5, 10, 8, 7.5, 5, 10, 10]
i=0
rating=PlayListRatings[0]

while rating >= 6:
    print(rating)
    i=i+1
    rating = PlayListRatings[i]
#I forgot to check for the end of the list if all the ratings were >=6

10
9.5
10
8
7.5

solution with the check

PlayListRatings = [10, 9.5, 10, 8, 7.5, 5, 10, 10]
i = 0
rating = PlayListRatings[0]
while(i < len(PlayListRatings) and rating >= 6):
    print(rating)
    i = i + 1 
    rating = PlayListRatings[i]  


    

Objectives
Understand Python loops.
How the loop Works
Learn about the needs for loop
Utilize Python's Range function.
Familiarize with Python's enumerate function.
Apply while loops for conditional tasks.
Distinguish appropriate loop selection.


FOR LOOPS:

# For loop example

dates = [1982,1980,1973]
N = len(dates)

for i in range(N):
    print(dates[i])     

for val in sequence:
      # statement(s) to be executed in sequence as a part of the loop.


We have a list of colours.

colors = ["red", "orange", "yellow", "green", "blue", "indigo", "violet"]


Let's print the colour name in the new line using for loop.

for color in colors:
    print(color)



Here is how you might use a for loop to count from 1 to 10:


for number in range(1, 11):
    print(number)

#9
for i in range(-5,6):
    print(i)
    
-5
-4
-3
-2
-1
0
1
2
3
4
5

#10
Genres=[ 'rock', 'R&B', 'Soundtrack', 'R&B', 'soul', 'pop']
for genre in Genres:
    print(genre)

rock
R&B
Soundtrack
R&B
soul
pop



#11
squares=['red', 'yellow', 'green', 'purple', 'blue']
for square in squares:
    print (square)


red
yellow
green
purple
blue


#12

Write a while loop to display the values of the Rating of an album playlist stored in the list PlayListRatings. 
If the score is less than 6, exit the loop. The list PlayListRatings is given by: 
PlayListRatings = [10, 9.5, 10, 8, 7.5, 5, 10, 10]

PlayListRatings = [10, 9.5, 10, 8, 7.5, 5, 10, 10]
i=0
rating=PlayListRatings[0]

while rating >= 6:
    print(rating)
    i=i+1
    rating = PlayListRatings[i]

10
9.5
10
8
7.5


PlayListRatings = [10, 9.5, 10, 8, 7.5, 5, 10, 10]
i = 0
rating = PlayListRatings[0]
while(i < len(PlayListRatings) and rating >= 6):
    print(rating)
    i = i + 1 
    rating = PlayListRatings[i]   


#13
Write a while loop to display the values of the Rating of an album playlist stored in the list PlayListRatings. If the score is less than 6, exit the loop. The list PlayListRatings is given by: PlayListRatings = [10, 9.5, 10, 8, 7.5, 5, 10, 10]

# Write your code below and press Shift+Enter to execute
PlayListRatings = [10, 9.5, 10, 8, 7.5, 5, 10, 10]
i=0
rating=PlayListRatings[0]

while rating >= 6:
    print(rating)
    i=i+1
    rating = PlayListRatings[i]


10
9.5
10
8
7.5


Write a while loop to copy the strings 'orange' of the list squares to the list new_squares. Stop and exit the loop if the value on the list is not 'orange':

squares = ['orange', 'orange', 'purple', 'blue ', 'orange']
new_squares = []
i=0;
#print(len(squares))
#print(i)
while( (i < len(squares)) and (squares[i]=="orange")):
    print(i)
    print(squares[i])
    new_squares.append('orange')
    print(new_squares[i])
    i = i + 1


0
orange
orange
1
orange
orange

Some real-life problems!
Your little brother has just learned multiplication tables in school. Today he has learned tables of 6 and 7. Help him memorise both the tables by printing them using for loop.

# Write your code here
i = 0
number = 6
for i in range(number):
  print( number, " X ", i,  " = ",  number*i) 
  i = i + 1

number = 7
for i in range(number):
  print( number, " X ", i,  " = ",  number*i) 
  i = i + 1


6  X  0  =  0
6  X  1  =  6
6  X  2  =  12
6  X  3  =  18
6  X  4  =  24
6  X  5  =  30
7  X  0  =  0
7  X  1  =  7
7  X  2  =  14
7  X  3  =  21
7  X  4  =  28
7  X  5  =  35
7  X  6  =  42

```python
print("Multiplication table of 6:")
for i in range (10):
    print("6*",i,"=",6*i)
print("Multiplication table of 7:")
for i in range (10):
    print("7*",i,"=",7*i)
    
```

</details>



The following is a list of animals in a National Zoo. Animals = ["lion", "giraffe", "gorilla", "parrots", "crocodile","deer", "swan"]

Your brother needs to write an essay on the animals whose names are made of 7 letters. Help him find those animals through a while loop and create a separate list of such animals.


# Write your code here
Animals = ["lion", "giraffe", "gorilla", "parrots", "crocodile","deer", "swan"]
SevenAnimals=[]
i = 0
#print(len(Animals[2]))
#print(len(Animals))
      
#while (i <= len(Animals)) and ((len(Animals[i])) == 7):
while (i <= (len(Animals)-1)):
    ThisAnimal = Animals[i]
    print(ThisAnimal," at ", i)
    if len(ThisAnimal) == 7:
        print(Animals[i])
        print(len(Animals[i]))
        print(i)
        SevenAnimals.append(Animals[i])
    i = i + 1
print(SevenAnimals)


lion  at  0
giraffe  at  1
giraffe
7
1
gorilla  at  2
gorilla
7
2
parrots  at  3
parrots
7
3
crocodile  at  4
deer  at  5
swan  at  6
['giraffe', 'gorilla', 'parrots']


With print statements commented out: 

Animals = ["lion", "giraffe", "gorilla", "parrots", "crocodile","deer", "swan"]
SevenAnimals=[]
i = 0
#print(len(Animals[2]))
#print(len(Animals))
      
#while (i <= len(Animals)) and ((len(Animals[i])) == 7):
while (i <= (len(Animals)-1)):
    ThisAnimal = Animals[i]
    #print(ThisAnimal," at ", i)
    if len(ThisAnimal) == 7:
        #print(Animals[i])
        #print(len(Animals[i]))
        #print(i)
        SevenAnimals.append(Animals[i])
    i = i + 1
print(SevenAnimals)

['giraffe', 'gorilla', 'parrots']



If given one argument (e.g., range(11)), it generates a sequence starting from 0 up to (but not including) the given number.

for number in range(11):
    print(number)


The Enumerated For Loop
Have you ever needed to keep track of both the item and its position in a list? An enumerated for loop comes to your rescue.
It's like having a personal assistant who not only hands you the item but also tells you where to find it.

Consider this example:

fruits = ["apple", "banana", "orange"]
for index, fruit in enumerate(fruits):
    print(f"At position {index}, I found a {fruit}")

With this loop, you not only get the fruit but also its position in the list. It's as if you have a magical guide pointing out each fruit's location!


# Example of for loop

for i in range(0, 8):
    print(i)

0
1
2
3
4
5
6
7


# Exmaple of for loop, loop through list
dates = [1982,1980,1973]
for year in dates:  
    print(year)   


1982
1980
1973

    
While Loops
count = 1
while count <= 10:
    print(count)
    count += 1


# Use for loop to change the elements in list

squares = ['red', 'yellow', 'green', 'purple', 'blue']

for i in range(0, 5):
    print("Before square ", i, 'is',  squares[i])
    squares[i] = 'white'
    print("After square ", i, 'is',  squares[i])

Before square  0 is red
After square  0 is white
Before square  1 is yellow
After square  1 is white
Before square  2 is green
After square  2 is white
Before square  3 is purple
After square  3 is white
Before square  4 is blue
After square  4 is white


# Loop through the list and iterate on both index and element value

squares=['red', 'yellow', 'green', 'purple', 'blue']

for i, square in enumerate(squares):
    print(i, square)




The Loop Flow
Both for and while loops have their special moves, but they follow a pattern:

Initialization: You set up things like a starting point or conditions.

Condition: You decide when the loop should keep going and when it should stop.

Execution: You do the task inside the loop.

Update: You make changes to your starting point or conditions to move forward.

Repeat: The loop goes back to step 2 until the condition is no longer true.


When to Use Each
For Loops: Use for loops when you know the number of iterations in advance and want to process each element in a sequence. They are best suited for iterating over collections and sequences where the length is known.

While Loops: Use while loops when you need to perform a task repeatedly as long as a certain condition holds true. While loops are particularly useful for situations where the number of iterations is uncertain or where you're waiting for a specific condition to be met.
    


Video: Functions (13:31)

Functions take an input and produce an output

Pyhhon has many built-in funcitons like "len()"m ::sum()"

Building functions in Python:
"""
add 1 to a      <=== documentation string 
"""
 def add1*a):
     b=a+1
    return b

if you use help(add1) it will print out the doc string 

def Mult(a,b):
    c=a*b
    return c


mult(2,3)

6


def MJ():                            <== this function returns the special "none" opject
    print( 'Michael Jackson')

def NoWork():
    pass
print(NoWork()_

None

def printStuff(Stuff):
    for i,s in enumerate(Stuff):

    print("Album", i, "Rating is ", s)

album_ratings - [10.0,8.5,9.5]
printStuff(album_ratings)


use the keyword "global" within a function to make a variable in the Global scope

def PinkFloyd():
    global ClaimedSales
    ClaimedSales = "45 million"
    return ClaimedSales


PinkFloyd()
print(ClaimedSales)
45 million



Exploring Python Functions
Estimated time needed: 15 minutes

Objectives:
By the end of this reading, you should be able to:

Describe the function concept and the importance of functions in programming
Write a function that takes inputs and performs tasks
Use built-in functions like len(), sum(), and others effectively
Define and use your functions in Python
Differentiate between global and local variable scopes
Use loops within the function
Modify data structures using functions


def calculate_total(a, b):  # Parameters: a and b
    total = a + b           # Task: Addition
    return total            # Output: Sum of a and b

result = calculate_total(5, 7)  # Calling the function with inputs 5 and 7
print(result)  # Output: 12

To use a built-in function, you simply call the function's name followed by parentheses. Any required arguments or parameters are passed into the function within these parentheses. The function then performs its predefined task and may return an output you can use in your code.

Here are a few examples of commonly used built-in functions:

len(): Calculates the length of a sequence or collection


string_length = len("Hello, World!")  # Output: 13
list_length = len([1, 2, 3, 4, 5])   # Output: 5
Copied!
sum(): Adds up the elements in an iterable (list, tuple, and so on)

total = sum([10, 20, 30, 40, 50])  # Output: 150
Copied!
max(): Returns the maximum value in an iterable

highest = max([5, 12, 8, 23, 16])  # Output: 23
Copied!
min(): Returns the minimum value in an iterable

lowest = min([5, 12, 8, 23, 16])  # Output: 5


Empty funtion

def function_name():
    pass


def greet(name):
    print("Hello, " + name)
result = greet("Alice")
print(result)  # Output: Hello, Alice

Docstrings (Documentation Strings)
Docstrings explain what a function does
Placed inside triple quotes under the function definition
Helps other developers understand your function
Example:


def multiply(a, b):
    """
    This function multiplies two numbers.
    Input: a (number), b (number)
    Output: Product of a and b
    """
    print(a * b)
multiply(2,6)



Return statement
Return gives back a value from a function
Ends the function's execution and sends the result
A function can return various types of data
Example:


def add(a, b):
    return a + b
sum_result = add(3, 5)  # sum_result gets the value 8



def print_numbers(limit):
    for i in range(1, limit+1):
        print(i)
print_numbers(5)  # Output: 1 2 3 4 5


def greet(name):
    return "Hello, " + name
for _ in range(3):
    print(greet("Alice"))


Modifying data structure using functions
You'll use Python and a list as the data structure for this illustration. In this example, you will create functions to add and remove elements from a list.

Part 1: Initialize an empty list
1
2
# Define an empty list as the initial data structure
my_list = []
Copied!
In this part, you start by creating an empty list named my_list. This empty list serves as the data structure that you will modify throughout the code.

Part 2: Define a function to add elements
1
2
3
# Function to add an element to the list
def add_element(data_structure, element):
    data_structure.append(element)
Copied!
Here, you define a function called add_element. This function takes two parameters:

data_structure: This parameter represents the list to which you want to add an element
element: This parameter represents the element you want to add to the list
Inside the function, you use the append method to add the provided element to the data_structure, which is assumed to be a list.

Part 3: Define a function to remove elements

# Function to remove an element from the list
def remove_element(data_structure, element):
    if element in data_structure:
        data_structure.remove(element)
    else:
        print(f"{element} not found in the list.")
Copied!
In this part, you define another function called remove_element. It also takes two parameters:

data_structure: The list from which we want to remove an element
element: The element we want to remove from the list
Inside the function, you use conditional statements to check if the element is present in the data_structure. If it is, you use the remove method to remove the first occurrence of the element. If it's not found, you print a message indicating that the element was not found in the list.

Part 4: Add elements to the list

# Add elements to the list using the add_element function
add_element(my_list, 42)
add_element(my_list, 17)
add_element(my_list, 99)
Copied!
Here, you use the add_element function to add three elements (42, 17, and 99) to the my_list. These are added one at a time using function calls.

Part 5: Print the current list

# Print the current list
print("Current list:", my_list)
Copied!
This part simply prints the current state of the my_list to the console, allowing us to see the elements that have been added so far.

Part 6: Remove elements from the list

# Remove an element from the list using the remove_element function
remove_element(my_list, 17)
remove_element(my_list, 55)  # This will print a message since 55 is not in the list
Copied!
In this part, you use the remove_element function to remove elements from the my_list. First, you attempt to remove 17 (which is in the list), and then you try to remove 55 (which is not in the list). The second call to remove_element will print a message indicating that 55 was not found.

Part 7: Print the updated list

# Print the updated list
print("Updated list:", my_list)
Copied!
Finally, you print the updated my_list to the console. This allows us to observe the modifications made to the list by adding and removing elements using the defined functions.



Functions in Python

Functions
What is a function?
Variables
Functions Make Things Simple
Pre-defined functions
Using if/else Statements and Loops in Functions
Setting default argument values in your custom functions
Global variables
Scope of a Variable
Collections and Functions
Quiz on Loops


You can define functions to provide the required functionality. Here are simple rules to define a function in Python:

Functions blocks begin def followed by the function name and parentheses ().
There are input parameters or arguments that should be placed within these parentheses.
You can also define parameters inside these parentheses.
There is a body within every function that starts with a colon (:) and is indented.
You can also place documentation before the body.
The statement return exits a function, optionally passing back a value.



# First function example: Add 1 to a and store as b

def add(a):
    """
    add 1 to a
    """
    b = a + 1
    print(a, "if you add one", b)
    return(b)

# Function example

def type_of_album(artist, album, year_released):
    
    print(artist, album, year_released)
    if year_released > 1980:
        return "Modern"
    else:
        return "Oldie"
    
x = type_of_album("Michael Jackson", "Thriller", 1980)
print(x)



# Print the list using for loop

def PrintList(the_list):
    for element in the_list:
        print(element)


#Compare Two Strings Directly using in operator
# add string
string= "Michael Jackson is the best"

# Define a funtion
def check_string(text):
    
# Use if else statement and 'in' operatore to compare the string
    if text in string:
        return 'String matched'
    else:
        return 'String not matched'

check_string("Michael Jackson is the best")


#Compare two strings using == operator and function
def compareStrings(x, y):
# Use if else statement to compare x and y
    if x==y:
        return 1
    
# Declare two different variables as string1 and string2 and pass string in it
string1 = "Michael Jackson is the best"
string2 = "Michael Jackson is the best"

# Declare a variable to store result after comparing both the strings
check = compareStrings(string1, string2)

#Use if else statement to compare the string
if check==1:
    print("\nString Matched")
else:
    print("\nString not Matched")


Count the Frequency of Words Appearing in a String Using a Dictionary.

Find the count of occurence of any word in our string using python. This is what we are going to do in this section, count the number of word in a given string and print it.

Lets suppose we have a ‘string’ and the ‘word’ and we need to find the count of occurence of this word in our string using python. This is what we are going to do in this section, count the number of word in a given string and print it.

The first thing, we will do is define a function and and then create a list that will be empty initially.

Next, we will add a code to convert the string to a list. Python string has a split() method. It takes a string and some separator to return a list.

Now we will declare an empty dictionary.

Next we will add code using for loop to iterate the words and value will will count the frequency of each words in the string and store them to the dictionary.

Finally we will print the dictionary.


# Python Program to Count words in a String using Dictionary
def freq(string):
    
    #step1: A list variable is declared and initialized to an empty list.
    words = []
    
    #step2: Break the string into list of words
    words = string.split() # or string.lower().split()
    
    #step3: Declare a dictionary
    Dict = {}
    
    #step4: Use for loop to iterate words and values to the dictionary
    for key in words:
        Dict[key] = words.count(key)
        
    #step5: Print the dictionary
    print("The Frequency of words is:",Dict)
    
#step6: Call function and pass string in it
freq("Mary had a little lamb Little lamb, little lamb Mary had a little lamb.Its fleece was white as snow And everywhere that Mary went Mary went, Mary went \
Everywhere that Mary went The lamb was sure to go")

    

Setting default argument values in your custom functions
You can set a default value for arguments in your function. For example, in the isGoodRating() function, what if we wanted to create a threshold for what we consider to be a good rating? Perhaps by default, we should have a default rating of 4:

# Example for setting param with default value

def isGoodRating(rating=4): 
    if(rating < 7):
        print("this album sucks it's rating is",rating)
        
    else:
        print("this album is good its rating is",rating)


# Test the value with default value and with input

isGoodRating()
isGoodRating(10)


Count the Frequency of Words Appearing in a String Using a Dictionary.

Find the count of occurence of any word in our string using python. This is what we are going to do in this section, count the number of word in a given string and print it.

Lets suppose we have a ‘string’ and the ‘word’ and we need to find the count of occurence of this word in our string using python. This is what we are going to do in this section, count the number of word in a given string and print it.

The first thing, we will do is define a function and and then create a list that will be empty initially.

Next, we will add a code to convert the string to a list. Python string has a split() method. It takes a string and some separator to return a list.

Now we will declare an empty dictionary.

Next we will add code using for loop to iterate the words and value will will count the frequency of each words in the string and store them to the dictionary.

Finally we will print the dictionary.




# Python Program to Count words in a String using Dictionary
def freq(string):
    
    #step1: A list variable is declared and initialized to an empty list.
    words = []
    
    #step2: Break the string into list of words
    words = string.split() # or string.lower().split()
    
    #step3: Declare a dictionary
    Dict = {}
    
    #step4: Use for loop to iterate words and values to the dictionary
    for key in words:
        Dict[key] = words.count(key)
        
    #step5: Print the dictionary
    print("The Frequency of words is:",Dict)
    
#step6: Call function and pass string in it
freq("Mary had a little lamb Little lamb, little lamb Mary had a little lamb.Its fleece was white as snow And everywhere that Mary went Mary went, Mary went \
Everywhere that Mary went The lamb was sure to go")



The Frequency of words is: {'Mary': 6, 'had': 2, 'a': 2, 'little': 3, 'lamb': 3, 'Little': 1, 'lamb,': 1, 'lamb.Its': 1, 'fleece': 1, 'was': 2, 'white': 1, 'as': 1, 'snow': 1, 'And': 1, 'everywhere': 1, 'that': 2, 'went': 3, 'went,': 1, 'Everywhere': 1, 'The': 1, 'sure': 1, 'to': 1, 'go': 1}


# Example of global variable

myFavouriteBand = "AC/DC"

def getBandRating(bandname):
    if bandname == myFavouriteBand:
        return 10.0
    else:
        return 0.0

print("AC/DC's rating is:", getBandRating("AC/DC"))
print("Deep Purple's rating is:",getBandRating("Deep Purple"))
print("My favourite band is:", myFavouriteBand)


AC/DC's rating is: 10.0
Deep Purple's rating is: 0.0
My favourite band is: AC/DC


# Example of global variable and local variable with the same name

myFavouriteBand = "AC/DC"

def getBandRating(bandname):
    myFavouriteBand = "Deep Purple"
    if bandname == myFavouriteBand:
        return 10.0
    else:
        return 0.0

print("AC/DC's rating is:",getBandRating("AC/DC"))
print("Deep Purple's rating is: ",getBandRating("Deep Purple"))
print("My favourite band is:",myFavouriteBand)



Collections and Functions¶
When the number of arguments are unknown for a function, They can all be packed into a tuple as shown:

def printAll(*args): # All the arguments are 'packed' into args which can be treated like a tuple
    print("No of arguments:", len(args)) 
    for argument in args:
        print(argument)
#printAll with 3 arguments
printAll('Horsefeather','Adonis','Bone')
#printAll with 4 arguments
printAll('Sidecar','Long Island','Mudslide','Carriage')


Similarly, The arguments can also be packed into a dictionary as shown:

def printDictionary(**args):
    for key in args:
        print(key + " : " + args[key])

printDictionary(Country='Canada',Province='Ontario',City='Toronto')


Country : Canada
Province : Ontario
City : Toronto


Functions can be incredibly powerful and versatile. They can accept (and return) data types, objects and even other functions as arguements. Consider the example below:

def addItems(list):
    list.append("Three")
    list.append("Four")

myList = ["One","Two"]

addItems(myList)

myList




----

Write a function code to find total count of word little in the given string: "Mary had a little lamb Little lamb, little lamb Mary had a little lamb.Its fleece was white as snow And everywhere that Mary went Mary went, Mary went Everywhere that Mary went The lamb was sure to go"**

# Write your code below and press Shift+Enter to execute
poem = ("Mary had a little lamb Little lamb, little lamb Mary had a little lamb.Its fleece was white as snow And everywhere that Mary went Mary went, Mary went Everywhere that Mary went The lamb was sure to go")
words=[]
i=0
theword = "little"
count=0

words = poem.lower().split()
#print(words[3])
#print(words)
for word in words:
    #print(word)
    #print("i =",i)
    if word == theword:
        count=count + 1
    i = i +1
print(count)


-----

Click here for the solution
# Python Program to Count words in a String using Dictionary
def freq(string,passedkey):

    #step1: A list variable is declared and initialized to an empty list.
    words = []

    #step2: Break the string into list of words
    words = string.split() # or string.lower().split()

    #step3: Declare a dictionary
    Dict = {}

    #step4: Use for loop to iterate words and values to the dictionary
    for key in words:
        if(key == passedkey):
            Dict[key] = words.count(key)   
    #step5: Print the dictionary
    print("Total Count:",Dict)

#step6: Call function and pass string in it
freq("Mary had a little lamb Little lamb, little lamb Mary had a little lamb.Its fleece was white as snow And everywhere that Mary went Mary went, Mary went \
Everywhere that Mary went The lamb was sure to go","little")
    

    
