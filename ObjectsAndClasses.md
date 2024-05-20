Objects and Classes Video notes

Every object has:
- A tupe
- An internal data representation (a blueprint)
- a set of procedures for interacting with the object (method)
An object is an instance of apraticular type

everytime we create an int or a list we are creating an object of the type int or list etc. 

We can find out the type of an object by using the command type()

Methods 
A class or type's methods are functions 
that every instance of that class or type provides. 

Sorting is an example of a method that interacts with the data in the object


 Create a ckass wuth one method - set_salary
 
 class Employee:
     def set_salary(self. value):
         self.salary = value 


 Then create an instance of the class "e" and set the salary to 2000

 e = Employee()
 e.set_salary(2000)
 print(e.salary)    #the resuls is (2000)


  why does the set_salary method have 2 parameters, but when I call the method 
  I only have to pass one arguement? 

 Answer:
 In the class, set_salary is an attribute (an attribute that holds a function object)
 e is a class instance

 when you call e.set_salary - python takes th instance and searches for its class (Employee) 
     next it searches in the class for a function object cakked set_salary
     now there is a pointer to e
     and a pointer to set_salary
       They both get packed into a method object 
         the argument list contains e and 2000
          next Python calls the set_salary function with e automatically added into the "self" and 2000 gets 
          inserte into the value parameter. i.e. Python automatically calls the method with the instance 
          insertedinto the first attribute (self, 2000)

          "self" is the instance itself. 

Classes
A class is a blueprint or template for creating objects. It defines the structure and behavior that its objects will have.
Think of a class as a cookie cutter and objects as the cookies cut from that template.
In Python, you can create classes using the class keyword.

Creating classes
When you create a class, you specify the attributes(data) and methods (functions) that objects of that class will have.
Attributes are defined as variables within the class, and methods are defined as functions.
For example,you can design a "Car" class with attributes such as "color" and "speed," along with methods like "accelerate."
          
Instantiating objects
Once you've defined a class, you can create individual objects (instances) based on that class.
Each object is independent and has its own set of attributes and methods.
To create an object, you use the class name followed by parentheses, so: "my_car = Car()"
 

Class declaration (class ClassName)
The class keyword is used to declare a class in Python.
ClassName is the name of the class, typically following CamelCase naming conventions.

class ClassName:
    # Class attributes (shared by all instances)
    class_attribute = value

Interacting with objects
You interact with objects by calling their methods or accessing their attributes using dot notation.

For example, if you have a Car object named my_car, you can set its color with my_car.color = "blue" and accelerate it with my_car.accelerate() if there's an accelerate method defined in the class.

Constructor method (def init(self, attribute1, attribute2, …):)
The __init__ method is a special method known as the constructor.
It initializes the instance attributes (also called instance variables) when an object is created.
The self parameter is the first parameter of the constructor, referring to the instance being created.
attribute1, attribute2, and so on are parameters passed to the constructor when creating an object.
Inside the constructor, self.attribute1, self.attribute2, and so on are used to assign values to instance attributes.

 class ClassName:
    # Class attributes (shared by all instances)
    class_attribute = value
    
    # Constructor method (initialize instance attributes)
    def __init__(self, attribute1, attribute2, ...):
         self.attribute1 = attribute1
        self.attribute2 = attribute2
        # ...
    
    # Instance methods (functions)
    def method1(self, parameter1, parameter2, ...):
        # Method logic
        pass
    def method2(self, parameter1, parameter2, ...):
        # Method logic
        pass


Real-world example
Let's write a python program that simulates a simple car class, allowing you to create car instances, accelerate them, and display their current speeds.

Let's start by defining a Car class that includes the following attributes and methods:
Class attribute max_speed, which is set to 120 km/h.

Constructor method __init__ that takes parameters for the car's make, model, color, and an optional speed (defaulting to 0). This method initializes instance attributes for make, model, color, and speed.

Method accelerate(self, acceleration) that allows the car to accelerate. If the acceleration does not exceed the max_speed, update the car's speed attribute. Otherwise, set the speed to the max_speed.

Method get_speed(self) that returns the current speed of the car.

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
class Car:
    # Class attribute (shared by all instances)
    max_speed = 120  # Maximum speed in km/h
    # Constructor method (initialize instance attributes)
    def __init__(self, make, model, color, speed=0):
        self.make = make
        self.model = model
        self.color = color
        self.speed = speed  # Initial speed is set to 0
    # Method for accelerating the car
    def accelerate(self, acceleration):
        if self.speed + acceleration <= Car.max_speed:
            self.speed += acceleration
        else:
            self.speed = Car.max_speed
    # Method to get the current speed of the car
    def get_speed(self):
        return self.speed
Copied!
Now, you will instantiate two objects of the Car class, each with the following characteristics:
car1: Make = "Toyota", Model = "Camry", Color = "Blue"

car2: Make = "Honda", Model = "Civic", Color = "Red"

# Create objects (instances) of the Car class
car1 = Car("Toyota", "Camry", "Blue")
car2 = Car("Honda", "Civic", "Red")

Using the accelerate method, you will increase the speed of car1 by 30 km/h and car2 by 20 km/h.

# Accelerate the cars
car1.accelerate(30)
car2.accelerate(20)

Lastly, you will display the current speed of each car by utilizing the get_speed method.

# Print the current speeds of the cars
print(f"{car1.make} {car1.model} is currently at {car1.get_speed()} km/h.")
print(f"{car2.make} {car2.model} is currently at {car2.get_speed()} km/h.")


Next steps
In conclusion, this reading provides a fundamental understanding of objects and classes in Python, essential concepts in object-oriented programming. Classes serve as blueprints for creating objects, encapsulating data attributes and methods. Objects represent real-world entities and possess their unique state and behavior. The structured code example presented in the reading outlines the key elements of a class, including class attributes, the constructor method for initializing instance attributes, and instance methods for defining object-specific functionality.

In the upcoming laboratory session, you can apply the concepts of objects and classes to gain hands-on experience.

-----LAB-------

Creating a Class

Now we are going to create a class Circle, but first, we are going to import a library to draw the objects:

# Import the library

import matplotlib.pyplot as plt
%matplotlib inline  

Figure 4: Creating a class Circle.

The next step is a special method called a constructor __init__, which is used to initialize the object. The inputs are data attributes. The term self contains all the attributes in the set. For example the self.color gives the value of the attribute color and self.radius will give you the radius of the object. We also have the method add_radius() with the parameter r, the method adds the value of r to the attribute radius. To access the radius we use the syntax self.radius. The labeled syntax is summarized in Figure 5:


# Create a class Circle

class Circle(object):
    
    # Constructor
    def __init__(self, radius=3, color='blue'):
        self.radius = radius
        self.color = color 
    
    # Method
    def add_radius(self, r):
        self.radius = self.radius + r
        return(self.radius)
    
    # Method
    def drawCircle(self):
        plt.gca().add_patch(plt.Circle((0, 0), radius=self.radius, fc=self.color))
        plt.axis('scaled')
        plt.show() 

Creating an instance of a class Circle¶

Let’s create the object RedCircle of type Circle to do the following:


# Create an object RedCircle

RedCircle = Circle(10, 'red')


We can use the <code>dir</code> command to get a list of the object's methods. Many of them are default Python methods.

# Find out the methods can be used on the object RedCircle

dir(RedCircle)

['__class__',
 '__delattr__',
 '__dict__',
 '__dir__',
 '__doc__',
 '__eq__',
 '__format__',
 '__ge__',
 '__getattribute__',
 '__getstate__',
 '__gt__',
 '__hash__',
 '__init__',
 '__init_subclass__',
 '__le__',
 '__lt__',
 '__module__',
 '__ne__',
 '__new__',
 '__reduce__',
 '__reduce_ex__',
 '__repr__',
 '__setattr__',
 '__sizeof__',
 '__str__',
 '__subclasshook__',
 '__weakref__',
 'add_radius',
 'color',
 'drawCircle',
 'radius']


We can look at the data attributes of the object:

# Print the object attribute radius

RedCircle.radius


10


# Print the object attribute color

RedCircle.color


'red'


We can change the object's data attributes:

# Set the object attribute radius

RedCircle.radius = 1
RedCircle.radius

1


We can draw the object by using the method drawCircle():

# Call the method drawCircle

RedCircle.drawCircle()

We can increase the radius of the circle by applying the method <code>add_radius()</code>. Let's increases the radius by 2 and then by 5:

# Use method to change the object attribute radius

print('Radius of object:',RedCircle.radius)
RedCircle.add_radius(2)
print('Radius of object of after applying the method add_radius(2):',RedCircle.radius)
RedCircle.add_radius(5)
print('Radius of object of after applying the method add_radius(5):',RedCircle.radius)


Radius of object: 1
Radius of object of after applying the method add_radius(2): 3
Radius of object of after applying the method add_radius(5): 8

Let’s create a blue circle. As the default colour is blue, all we have to do is specify what the radius is:


# Create a blue circle with a given radius

BlueCircle = Circle(radius=100)

As before, we can access the attributes of the instance of the class by using the dot notation:

# Print the object attribute radius

BlueCircle.radius

100

# Print the object attribute color

BlueCircle.color

'blue'

We can draw the object by using the method drawCircle():


# Call the method drawCircle

BlueCircle.drawCircle()

The Rectangle Class

Let's create a class rectangle with the attributes of height, width, and color. We will only add the method to draw the rectangle object:



Task-5. Additionally, you need to create two objects of the Vehicle class object that should have a max speed of 200kph and mileage of 50000kmpl with five seating capacities, and another car object should have a max speed of 180kph and 75000kmpl with four seating capacities.


#Type your code here
class Car:
    # Class attribute (shared by all instances)
    max_speed = 120  # Maximum speed in km/h
    mileage = 0
    color = 'white'
    seating_capacity = 2
    
    # Constructor method (initialize instance attributes)
#    def __init__(self, mileage, make, model, color, speed=0):
    def __init__(self, max_speed, mileage):
        self.mileage = mileage
        self.max_speed = max_speed
#        self.make = make
#        self.model = model
#        self.color = color
#        self.speed = speed  # Initial speed is set to 0
        self.seating_capacity = None 
    # Method to set the current seating capacity of the car
    def assign_seating_capacity(self, seating_capacity):
        self.seating_capacity = seating_capacity
        
    # Method to print the current properties of the car
    def print_properties(self):
  #      print(self.make)
        print(self.max_speed)
        print(self.mileage)
        print(self.seating_capacity)



car1=Car("200kph", "50000kmpl")
car2=Car("180kph", "75000kmpl")

car1.assign_seating_capacity(5)
car2.assign_seating_capacity(4)
# print(car1.max_speed)
car2.print_properties()
car1.print_properties()



180kph
75000kmpl
4
200kph
50000kmpl
5
