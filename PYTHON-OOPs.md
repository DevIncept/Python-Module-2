https://2.bp.blogspot.com/-7Fj1bZ4UAfM/W0EIT1Ts7JI/AAAAAAAAAl4/-E7205nyxC8XRYtH8z2d5B9aeL2sMjPpQCLcBGAs/s1600/Polymorphism_In_Csharp.png<p align="center">
   <img src="https://miro.medium.com/max/1200/1*PPIp7twJJUknfohZqtL8pQ.png" alt="Python Programming"
        width="500" height="150">
   <br />
    <b> OOPS IN PYTHON </b>   
   <br />
   <b> This mark down file helps to understand OOPS Concept in PYTHON. </b>
   <br />
</p>

---


# 📋 Python OOPs Concept

#### What Is Object-Oriented Programming?
<p align="justify">
    Object-Oriented Programming(OOP), is all about creating “objects”. An object is a group of interrelated variables and functions. These variables are often referred to as properties of the object and functions are referred to as the behavior of the objects. These objects provide a better and clear structure for the program.

For example, a car can be an object. If we consider the car as an object then its properties would be – its color, its model, its price, its brand, etc. And its behavior/function would be acceleration, slowing down, gear change.

Another example- If we consider a dog as an object then its properties would be- his color, his breed, his name, his weight, etc. And his behavior/function would be walking, barking, playing, etc.

Object-Oriented programming is famous because it implements the real-world entities like objects, hiding, inheritance, etc in programming. It makes visualization easier because it is close to real-world scenarios.

Like other general-purpose programming languages, Python is also an object-oriented language since its beginning. It allows us to develop applications using an Object-Oriented approach. In Python, we can easily create and use classes and objects.
An object-oriented paradigm is to design the program using classes and objects. The object is related to real-word entities such as book, house, pencil, etc. The oops concept focuses on writing the reusable code. It is a widespread technique to solve the problem by creating objects.    

 </p>
Major principles of object-oriented programming system are given below.

  - Class
  - Object
  - Method
  - Inheritance
  - Polymorphism
  - Data Abstraction
  - Encapsulation
  <p align="center">
<img src="https://onlineitguru.com/storage/course_files/1609476851_Python%20OOPs%20concepts.png" alt="Python Programming"width="500" height="150"> 
  </p>  
  
 ---
 

## 📋Class
<p align="justify">
The class can be defined as a collection of objects. It is a logical entity that has some specific attributes and methods. For example: if you have an employee class, then it should contain an attribute and method, i.e. an email id, name, age, salary, etc. Class is a user-defined data type which binds data and functions.
It’s the blueprint or design of any object where we intiliaze the necessary parameters to construct our object.

  - Functions inside class is called as Methods
  - It’s good to start a class name with an upper case alphabet (not a necessary condition) and followed by some mthods.    

To create a class, use the keyword  _*class*_, followed by the name of the class name and ending with a colon. Identation level tells where the class ends.
                   
#### Syntax
```python   
class Classname:
      methods():
      <statements>
``` 
### How to create an empty class?         
```python
class Classname:  
     pass 
```          
Here we have created a empty class without any members by just using the keyword pass within it.
##### Example 1
```python
class Point:
  pass
print(Point)
```          
 The output would be –
<class '__main__.Point'>
The term __main__ indicates that the class Point is in the main scope of current module, i.e class Point is at the top level while executing the program.

Create a class named MyClass, with a property named x:
```python  
    class MyClass:
        x = 5
```   
##### Example 2 
```python
 class Employee:
     empNum=123    #class variable
     
     def display(self):   #class method definition
         print(self.empNum)
```     
Variables defined in class are called *class variables* and functions defined inside a class are called class methods. Class variables class methods are together known as class members. The class members can be accesssed through class objects. Class methods have access to all the data contained in the instaance of object.
self represents the instance of the class. By using the “self” keyword we can access the attributes and methods of the class in python. It binds the attributes with the given arguments.    
</p>
          
---
          

## 📋 Objects
<p align="justify">
An object is an instance of a class. It has physical existence. One can create any number of objects for a class.
The object is an entity that has state and behavior. It may be any real-world object like the mouse, keyboard, chair, table, pen, etc.

Everything in Python is an object, and almost everything has attributes and methods. All functions have a built-in attribute __doc__, which returns the docstring defined in the function source code.

When we define a class, it needs to create an object to allocate the memory.
An object has two characteristics:
1. attributes
2. behavior
Let's take an example:
A parrot is an object, as it has the following properties:
- name, age, color as attributes
- singing, dancing as behavior    
<img src="https://sts.doit.wisc.edu/manuals/python2/images/OOP_Example.jpg" alt="Python Programming" width="500" height="150"> 
      

    
### Syntax
```python    
class Classname:
  methods():
    <statements>
   
c1 = Classname()
c2 = Classname()     # c1 and c2 are the objects of the "Classname"
```        
Consider the following example:
```python
class Point:
   pass 
p=Point()     #first object
print(p)    
```
Point object is created.
A reference is assigned to the object p.
Creating a new object is called as instantiation and the object is instance of a
class.
print an object, class it belongs to and where it is stored in the memory.
The output would be –
```    
<__main__.Point object at 0x003C1BF0>
```
Since our class was empty, it returns the address where the object is stored i.e 0x003C1BF0.
     
##### Example 2:
```python
class MyClass:
  x = 5  
p1 = MyClass()         #Created an object named p1, and print the value of x:
print(p1.x)
```  
Note: Three important things to remember are-
  - You can create any number of objects of a class.
  - If the method requires n parameters and you do not pass the same number of arguments then an error will occur.
  - Order of the arguments matters.    
</p>  
        
---
        

### The _ _init_ _ ( ) function
<p align="justify">
To understand the meaning of classes we have to understand the built-in __init__() function.
All classes have a function called __init__(), which is always executed when the class is being initiated.
Use the __init__() function to assign values to object properties, or other operations that are necessary to do when the object is being created.
This __init__() method is also known as the constructor method. We call a constructor method whenever an object of the class is constructed.
The job of the class constructor is to assign the values to the data members of the class when an object of the class is created.

There can be various properties of a car such as its name, color, model, brand name, engine power, weight, price, etc. We’ll choose only a few for understanding purposes.
```python
class Car:
    def __init__(self, name, color):
        self.name = name
        self.color = color
```
So, the properties of the car or any other object must be inside a method that we call __init__( ). 
Now let’s talk about the parameter of the __init__() method. So, the first parameter of this method has to be self. Then only will the rest of the parameters come.

The two statements inside the constructor method are –

1. self.name = name
2. self.color = color

This will create new attributes namely name and color and then assign the value of the respective parameters to them. The “self” keyword represents the instance of the class. By using the “self” keyword we can access the attributes and methods of the class. It is useful in method definitions and in variable initialization. The “self” is explicitly used every time we define a method.

Note: You can create attributes outside of this __init__() method also. But those attributes will be universal to the whole class and you will have to assign the value to them.

Suppose all the cars in your showroom are Sedan and instead of specifying it again and again you can fix the value of car_type as Sedan by creating an attribute outside the __init__().
```python
class Car:
    car_type = "Sedan"                 #class attribute
    def __init__(self, name, color):
        self.name = name               #instance attribute   
        self.color = color             #instance attribute
```
Here, Instance attributes refer to the attributes inside the constructor method i.e self.name and self.color. And, Class attributes refer to the attributes outside the constructor method i.e car_type.
</p>

---


## 📋 Methods
<p align="justify">
Methods are the functions that we use to describe the behavior of the objects. They are also defined inside a class. The method is a function that is associated with an object. In Python, a method is not unique to class instances. Any object type can have methods.The method is a function that is associated with an object. In Python, a method is not unique to class instances. Any object type can have methods. Methods in objects are functions that belong to the object.
In simple way,Functions inside the class are called as Methods.

#### Example
```python
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def myfunc(self):
    print("Hello my name is " + self.name)

p1 = Person("John", 36)
p1.myfunc()
```
Output:
Hello my name is John    
    
The methods defined inside a class other than the constructor method are known as the instance methods. Furthermore, we have one instance method here- myfunc(). This method has no additional parameter. This method is using the instance attributes.
</p>  

---


## 📋 Inheritance
<p align="justify">
Inheritance is the most important aspect of object-oriented programming, which simulates the real-world concept of inheritance. The method of inheriting the properties of parent class into a child class is known as inheritance. 
Inheritance is the procedure in which one class inherits the attributes and methods of another class.  The class whose properties and methods are inherited is known as Parent class. And the class that inherits the properties from the parent class is the Child class.

The interesting thing is, along with the inherited properties and methods, a child class can have its own properties and methods.  
Following are the benefits of inheritance.
- Code reusability- we do not have to write the same code again and again, we
  can just inherit the properties we need in a child class.
- It represents a real world relationship between parent class and child class.
- It is transitive in nature. If a child class inherits properties from a parent
  class, then all other sub-classes of the child class will also inherit the
  properties of the parent class. 

### Syntax
```python    
class parent_class:
body of parent class

class child_class( parent_class):
body of child class  
```  
By using inheritance,we can create a class which uses all the properties and behaviour of another class. The new class is also known as derived class or child class, and the one whose properties are acquired is known as base class or parent class.
### Example
```python 
class Parent:
    def first(self):
      print('fisrt function')
class Child(Parent):
    def second(self):
      print('second function')
ob=child()
ob.first()
ob.second()
```    
 Output:
 first function
 second function   
    
#### Types of Inheritance
1. Single Inheritance
2. Multi level Inheritance
3. Multiple Inheritance
4. Hierarchical Inheritance
5. Hybrid Inheritance

 <img src="https://static.javatpoint.com/tutorial/typescript/images/typescript-classes-types-of-inheritance.png" alt="Python Programming" width="500" height="150"> 

#### Sub-classing 
Calling a constructor of the parent class by mentioning the parent class name in the
declaration of the child class is known as sub-classing. A child class identifies its parent
class by sub-classing.
    
#### _ _init_ _( ) Function
The __init__() function is called every time a class is being used to make an object.
The child class will no longer be able to inherit the parent class’s __init__() function.
The child’s class __init__() function overrides the parent class’s __init__() function.
 
```python
class Parent:
    def __init__(self , fname):
        self.firstname = fname
    def view(self):
         print(self.firstname)
class Child(Parent):
    def __init__(self, fname):
        Parent.__init__(self,fname)
    def view(self):
         print("course name", self.firstname)
ob=Child("Python")
ob.view()
```
 Output:
    ('course name', 'Python')
    
#### 1. Single Inheritance :
    When a child class inherits only a single parent class.    
 #### Example
```python
class Parent:
     def func1(self):
          print("This function is in parent class.")
class Child(Parent):
     def func2(self):
          print("This function is in child class.")
object = Child()
object.func1()
object.func2()    
```    
#### 2. Multi Level Inheritance :
    In multilevel inheritance, features of the base class and the derived class are further inherited into the new derived class. This is similar to a relationship representing a child and grandfather. 
 
  #### Example
```python
class Parent:
     def func1(self):
          print("This is function 1.")
class Child(Parent):
     def func2(self):
          print("This is function 2.")
class Child2(Child):
     def func3(self):
          print("This is function 3.")    
ob = Child2()
ob.func1()
ob.func2()    
ob.func3()     
```    
#### 3 . Multiple Inheritance :
    When a child class inherits from more than one parent class.
 #### Example
```python
class Parent:
     def func1(self):
          print("This is function 1.")
class Parent2:
     def func2(self):
          print("This is function 2.")    
class Child(Parent,Parent2):
     def func3(self):
          print("This is function 3.")   
ob = Child()
ob.func1()
ob.func2()    
ob.func3()     
```    
        
#### 4 . Hierarchical Inheritance :  
    When more than one derived classes are created from a single base this type of inheritance is called hierarchical inheritance. In this program, we have a parent (base) class and two child (derived) classes.
#### Example
```python    
class Parent:
      def func1(self):
          print("This function is in parent class.")
class Child1(Parent):
      def func2(self):
          print("This function is in child 1.")
class Child2(Parent):
      def func3(self):
          print("This function is in child 2.")
object1 = Child1()
object2 = Child2()
object1.func1()
object1.func2()
object2.func1()
object2.func3()    
```
#### 5 . Hybrid Inheritance : 
    Inheritance consisting of multiple types of inheritance is called hybrid inheritance.
 #### Example
```python
class School:
     def func1(self):
         print("This function is in school.")
class Student1(School):
     def func2(self):
         print("This function is in student 1. ")
class Student2(School):
     def func3(self):
         print("This function is in student 2.")
class Student3(Student1, School):
     def func4(self):
         print("This function is in student 3.")
object = Student3()
object.func1()
object.func2() 
```    
</p>    

---


## 📋 Polymorphism
<p align="justify">
The word polymorphism means having many forms. In programming, polymorphism means same function name (but different signatures) being uses for different types. 
    
Polymorphism contains two words "poly" and "morphs". Poly means many, and morph means shape. By polymorphism, we understand that one task can be performed in different ways. For example - you have a class animal, and all animals speak. But they speak differently. Here, the "speak" behavior is polymorphic in a sense and depends on the animal. So, the abstract "animal" concept does not actually "speak", but specific animals (like dogs and cats) have a concrete implementation of the action "speak".
In OOP it refers to the functions having the same names but carrying different functionalities.
    
#### What is the main purpose of polymorphism in Python?
Polymorphism means multiple forms. In python we can find the same operator or function taking multiple forms. It also useful in creating different classes which will have class methods with same name. That helps in re using a lot of code and decreases code complexity.    
#### Advantages of Polymorphism
- It helps the programmer to reuse the codes, i.e., classes once written, tested and implemented can be reused as required. 
- Saves a lot of time.
- Single variable can be used to store multiple data types.
- Easy to debug the codes. 
<img src="https://2.bp.blogspot.com/-7Fj1bZ4UAfM/W0EIT1Ts7JI/AAAAAAAAAl4/-E7205nyxC8XRYtH8z2d5B9aeL2sMjPpQCLcBGAs/s1600/Polymorphism_In_Csharp.png" alt="Python Programming" width="500" height="150"> 
    
 
#### Example 1: Polymorphism in addition operator
We know that the + operator is used extensively in Python programs. But, it does not have a single usage.

For integer data types, + operator is used to perform arithmetic addition operation.
```python
num1 = 1
num2 = 2
print(num1+num2)    
```
Hence, the above program outputs 3.

Similarly, for string data types, + operator is used to perform concatenation.
```python
str1 = "Python"
str2 = "Programming"
print(str1+" "+str2)
```
As a result, the above program outputs Python Programming.

Here, we can see that a single operator + has been used to carry out different operations for distinct data types. This is one of the most simple occurrences of polymorphism in Python.

#### Function Polymorphism in Python
There are some functions in Python which are compatible to run with multiple data types.

One such function is the len() function. It can run with many data types in Python. Let's look at some example use cases of the function.

#### Example 2: Polymorphic len() function
```python    
print(len("Devincept"))
print(len(["Python", "Java", "C"]))
print(len({"Name": "John", "Address": "Nepal"}))
```
Output:
9
3
2
Here, we can see that many data types such as string, list, tuple, set, and dictionary can work with the len() function. However, we can see that it returns specific information about specific data types.
##### Polymorphism in len() function in Python
len():-
1. str   : Length of the string.
2. list  : Number of items.
3. dict  : Number of Keys.
    
#### Class Polymorphism in Python 
We can use the concept of polymorphism while creating class methods as Python allows different classes to have methods with the same name.
We can then later generalize calling these methods by disregarding the object we are working with. Let's look at an example:

##### Example 3: Polymorphism in Class Methods
```python    
class Cat:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    def info(self):
        print(f"I am a cat. My name is {self.name}. I am {self.age} years old.")
    def make_sound(self):
        print("Meow")
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    def info(self):
        print(f"I am a dog. My name is {self.name}. I am {self.age} years old.")
    def make_sound(self):
        print("Bark")
cat1 = Cat("Kitty", 2.5)
dog1 = Dog("Fluffy", 4)
for animal in (cat1, dog1):
    animal.make_sound()
    animal.info()
    animal.make_sound()
``` 
Here, we have created two classes Cat and Dog. They share a similar structure and have the same method names info() and make_sound().
However, notice that we have not created a common superclass or linked the classes together in any way. Even then, we can pack these two different objects into a tuple and iterate through it using a common animal variable. It is possible due to polymorphism.
    
</p> 

---


## 📋 Encapsulation
<p align="justify">
Using OOP in Python, we can restrict access to methods and variables. This prevents data from direct modification which is called encapsulation. In Python, we denote private attributes using underscore as the prefix i.e single _ or double __.    
Encapsulation is also an essential aspect of object-oriented programming. It is used to restrict access to methods and variables. In encapsulation, code and data are wrapped together within a single unit from being modified by accident. 
This puts restrictions on accessing variables and methods directly and can prevent the accidental modification of data. To prevent accidental change, an object’s variable can only be changed by an object’s method. Those types of variables are known as private variable. 
A class is an example of encapsulation as it encapsulates all the data that is member functions, variables, etc.
 

    

Consider a real-life example of encapsulation, in a company, there are different sections like the accounts section, finance section, sales section etc. The finance section handles all the financial transactions and keeps records of all the data related to finance. Similarly, the sales section handles all the sales-related activities and keeps records of all the sales. Now there may arise a situation when for some reason an official from the finance section needs all the data about sales in a particular month. In this case, he is not allowed to directly access the data of the sales section. He will first have to contact some other officer in the sales section and then request him to give the particular data. This is what encapsulation is. Here the data of the sales section and the employees that can manipulate them are wrapped under a single name “sales section”. Using encapsulation also hides the data. In this example, the data of the sections like sales, finance, or accounts are hidden from any other section.    
    
#### Benefits of Encapsulation in Python
Encapsulation not only ensures better data flow but also protects the data from outside sources. The concept of encapsulation makes the code self-sufficient. It is very helpful in the implementation level, as it prioritizes the ‘how’ type questions, leaving behind the complexities. You should hide the data in the unit to make encapsulation easy and also to secure the data.    
#### Methods to Control Access
There are multiple methods that are offered by Python to limit variable and method access across the program. Let’s go over the methods in detail.
##### Using Single Underscore
A common Python programming convention to identify a private variable is by prefixing it with an underscore. Now, this doesn’t really make any difference on the compiler side of things. The variable is still accessible as usual. But being a convention that programmers have picked up on, it tells other programmers that the variables or methods have to be used only within the scope of the class.

See the below example:
```python        
class Person:
    def __init__(self, name, age=0):
        self.name = name
        self._age = age

    def display(self):
        print(self.name)
        print(self._age)

person = Person('Dev', 30)
#accessing using class method
person.display()
#accessing directly from outside
print(person.name)
print(person._age)    
```
##### Using Double Underscores
If you want to make class members i.e. methods and variables private, then you should prefix them with double underscores. But Python offers some sort of support to the private modifier. This mechanism is called Name mangling. With this, it is still possible to access the class members from outside it.
###### Name Mangling
In Python, any identifier with __Var is rewritten by a python interpreter as _Classname__Var, and the class name remains as the present class name. This mechanism of changing names is called Name Mangling in Python.
In the below example, in Class person, the age variable is changed and it’s prefixed by leading double underscores.
```python  
class Person:
    def __init__(self, name, age=0):
        self.name = name
        self.__age = age

    def display(self):
        print(self.name)
        print(self.__age)

person = Person('Dev', 30)
#accessing using class method
person.display()
#accessing directly from outside
print('Trying to access variables from outside the class ')
print(person.name)
print(person.__age)    
```      
#### Using Getter and Setter methods to access private variables
If you want to access and change the private variables, accessor (getter) methods and mutators(setter methods) should be used, as they are part of Class. Making Use of the setter method provides indirect access to the private class method. This is a clear example of encapsulation where we are restricting the access to private class method and then use the setter method to grant access.    

```python    
class Person:
    def __init__(self, name, age=0):
        self.name = name
        self.__age = age

    def display(self):
        print(self.name)
        print(self.__age)

    def getAge(self):
        print(self.__age)

    def setAge(self, age):
        self.__age = age

person = Person('Dev', 30)
#accessing using class method
person.display()
#changing age using setter
person.setAge(35)
person.getAge()
``` 
Output:
Dev 
30
35    
    
</p>

---

## 📋Data Abstraction
<p align="justify">
Abstraction is used to hide the internal functionality of the function from the users. The users only interact with the basic implementation of the function, but inner working is hidden. User is familiar with that "what function does" but they don't know "how it does".
In simple words, we all use the smartphone and very much familiar with its functions such as camera, voice-recorder, call-dialing, etc., but we don't know how these operations are happening in the background. Let's take another example - When we use the TV remote to increase the volume. We don't know how pressing a key increases the volume of the TV. We only know to press the "+" button to increase the volume.
That is exactly the abstraction that works in the object-oriented concept. 
Abstraction classes in Python
In Python, abstraction can be achieved by using abstract classes and interfaces.

A class that consists of one or more abstract method is called the abstract class. Abstract methods do not contain their implementation. Abstract class can be inherited by the subclass and abstract method gets its definition in the subclass. Abstraction classes are meant to be the blueprint of the other class. An abstract class can be useful when we are designing large functions. An abstract class is also helpful to provide the standard interface for different implementations of components. Python provides the abc module to use the abstraction in the Python program. Let's see the following syntax.

#### Syntax 
```python 
from abc import ABC  
class ClassName(ABC): 
```    
We import the ABC class from the abc module.
##### Abstract Base Classes
An abstract base class is the common application program of the interface for a set of subclasses. It can be used by the third-party, which will provide the implementations such as with plugins. It is also beneficial when we work with the large code-base hard to remember all the classes.

##### Working of the Abstract Classes
Unlike the other high-level language, Python doesn't provide the abstract class itself. We need to import the abc module, which provides the base for defining Abstract Base classes (ABC). The ABC works by decorating methods of the base class as abstract. It registers concrete classes as the implementation of the abstract base. We use the @abstractmethod decorator to define an abstract method or if we don't provide the definition to the method, it automatically becomes the abstract method. Let's understand the following example.
```python     
from abc import ABC  
class Polygon(ABC):   
   # abstract method   
   def sides(self):   
       pass  
class Triangle(Polygon):   
   def sides(self):   
      print("Triangle has 3 sides")   
class Pentagon(Polygon):       
  def sides(self):   
      print("Pentagon has 5 sides")   
class Hexagon(Polygon):   
  def sides(self):   
      print("Hexagon has 6 sides")   
class square(Polygon):   
  def sides(self):   
      print("I have 4 sides")   
t = Triangle()   
t.sides()  
s = square()   
s.sides()   
p = Pentagon()   
p.sides()   
k = Hexagon()   
K.sides() 
```    
Output:
Triangle has 3 sides
Square has 4 sides
Pentagon has 5 sides
Hexagon has 6 sides  

Explanation -
In the above code, we have defined the abstract base class named Polygon and we also defined the abstract method. This base class inherited by the various subclasses. We implemented the abstract method in each subclass. We created the object of the subclasses and invoke the sides() method. The hidden implementations for the sides() method inside the each subclass comes into play. The abstract method sides() method, defined in the abstract class, is never invoked. 

Below are the points which we should remember about the abstract base class in Python.
1. An Abstract class can contain the both method normal and abstract method.
2. An Abstract cannot be instantiated; we cannot create objects for the abstract class.
3. Abstraction is essential to hide the core functionality from the users. We have covered the all the basic concepts of Abstraction in Python.    
    
</p>    


## Key Points to Remember:

 - Object-Oriented Programming makes the program easy to understand as well as efficient.
 - Since the class is sharable, the code can be reused.
 - Data is safe and secure with data abstraction.
 - Polymorphism allows the same interface for different objects, so programmers can write efficient code.



```python

```
