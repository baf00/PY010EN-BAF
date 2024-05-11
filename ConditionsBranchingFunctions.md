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
    
