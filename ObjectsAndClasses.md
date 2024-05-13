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

          
          
 
 
  
 
         
