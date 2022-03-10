<p align="center">
   <img src="https://miro.medium.com/max/1200/1*PPIp7twJJUknfohZqtL8pQ.png" alt="Python Programming"
        width="600" height="200">
   <br />
   <b> CLASSES AND OBJECTS IN PYTHON</b>
   <br />
   
   <br />
</p>


# ***CLASSES AND OBJECTS IN PYTHON*** :heart:

***Python*** is an ***object oriented programming (OOP)*** language and it provides all the features required to support object-oriented programming .

***OOP*** mainly focuses on ***class and objects***.


## ***Class*** :loud_sound:

***Classes*** are defined by the ***user***. The ***class*** provides the ***basic structure for an objec***.***Class*** is a collection of ***data(variables) and methods(functions)***.A ***class*** can be defined as a ***blue print*** or a previously defined structure from which ***objects*** are made.

### ***NOTE :*** :bulb:
* In python, a class is defined by using keyword **"class"**.
* As soon as we **define a class**, the **interpreter** instantly creates an **object** that has the same name as the **class name.**
* **Attributes** are the **variables** that belong to **class.**
* **Attributes** are always **public** and can be accessed using **dot(.) operator.**

### ***Syntax*** :bookmark:

class class_name:

     statements

#### ***Example 1***  :computer:



```python
class age :
    x=10
print(age)
```

    <class '__main__.age'>
    

## ***Objects***

* An **object** is an **instace of a class** that has some **attributes and behaviour.**
* The **object** behaves according to the **class** of which it is an **object.**
* **Objects** can be used to access the **attributes of the class.**
 

### ***An object consists of :***

1. **State :** It is representated by **attributes of an object**. It also reflects the **properties of an object.**
2. **Behavior :** It is represented by **methods of an object.** It also reflects the response of an **object with other objects.**
3. **Identity :** It gives a **unique name** to an object and enables one object to **interact with other objects.**

### ***Syntax*** :bookmark:

obj_name = class_name()

#### ***Example*** :computer:



```python
class age :
    x=10
print(age)

age1 = age () #object instantiation
```

    <class '__main__.age'>
    

#### ***Example 2*** :computer:



```python
#sample class
class student :
    id = 100     #attribute
    name = "Mike" #attribute
    
    def display(self):  #a sample method
        print("ID : %d \nName : %s" %(self.id, self.name))
    
stud = student()  # creating an object of student class
stud.display()
```

    ID : 100 
    Name : Mike
    

**In the above example, an object is created which is basically student named stud. This class has two attributes that tells that stud has id 100 and name Mike.**

### ***NOTE :*** :bulb:

**The self parameter is a refrence to the current instance of the class, and is used to access variables that belongs to the class.**


### ***Self Parameter*** 

* Is similar to this **pointer in c++ and reference in java.**
* **Self** represents the **instance of the class.**


#### ***Example*** :computer:



```python
class Student:
    def say_marks(self):
        print("Argh! I scored 100!")
    def studies(self,hours):
        
        print("No_hrs:",hours,end="")

student1 = Student()

student1.say_marks()

hours = int(input())

student1.studies(hours)
```

    Argh! I scored 100!
    8
    No_hrs: 8

### ***__init__() function*** 

* **init method** is similar to **constructors in c++ and java.**
* Use of **init() function** to assign values to **object properties, or other operations** that are necessary to do when the object is being **created.**

#### ***Example 1*** :computer:



```python
class student:
    def __init__(name,school) :
        name.school = school

s1 = student("Mike")
print(s1.school)
```

    Mike
    

#### ***Example 2*** :computer:



```python
#this example shows to modify object proprties
class student:
    def __init__(name,school,city) :
        name.school = school
        name.city=city
    
    def func(name):
        print("Hello my name is " +name.school)

s1 = student("Mike", "Bangalore")
s1.func()
print(s1.school)
print("previous city of my school is ", s1.city)
s1.city= "Mysore"
print("new city of my school is", s1.city)
```

    Hello my name is Mike
    Mike
    previous city of my school is  Bangalore
    new city of my school is Mysore
    

#### ***Delete object properties***

 We can **delete properties on objects** by using **del keyword**


#### ***Example*** :computer:



```python
class student:
    def __init__(name,school,city) :
        name.school = school
        name.city=city
    
    def func(name):
        print("Hello my name is " +name.school)

s1 = student("Mike", "Bangalore")
del s1
print(s1.school)
#having an empty class definition like this, would raise an error without the pass statement.
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-7-88ab8982e316> in <module>
          9 s1 = student("Mike", "Bangalore")
         10 del s1
    ---> 11 print(s1.school)
         12 #having an empty class definition like this, would raise an error without the pass statement.
    

    NameError: name 's1' is not defined


#### ***Objects are mutable*** :bulb:

- The **state of an object** can be **changed at any point of time by making changes to its attributes.**


**Now let's look into calculator example using classes and objects.** :heavy_plus_sign:


```python
class Calculator:
    def sum(self,sum_list):
        sum=0
        for i in range(0,len(sum_list)):
            sum=sum+sum_list[i]
        return sum
    def minus(self,first,second):
       
        return first-second
    def multiply(self,sum_list):
        d=1
        for i in range(0,len(sum_list)):
            
            d=d*sum_list[i]
        return d
    def divide(self,fourth,fifth):
        if(fifth==0):
            return "Div by 0 not allowed!"
        else:
            b=fourth//fifth
            return b
        
calc = Calculator()
print("Enter your numbers for calculation")
first = int(input())
second = int(input())
third = int(input())
fourth = int(input())
fifth = int(input())

sum_list = [first,second,third,fourth,fifth]
answer_1 = calc.sum(sum_list)
print(f"Sum of {sum_list} is {answer_1}")

answer_2 = calc.minus(first,second)
print(f"{first} - {second} = {answer_2}")

answer_3 = calc.multiply(sum_list[:-1]) # selecting only first 4 values
print(f"Multiplying {sum_list[:-1]} = {answer_3}")

answer_4 = calc.divide(fourth,fifth)
print(f"Dividing {fourth}/{fifth} = {answer_4}")
```

    Enter your numbers for calculation
    89
    56
    54
    123
    69
    Sum of [89, 56, 54, 123, 69] is 391
    89 - 56 = 33
    Multiplying [89, 56, 54, 123] = 33103728
    Dividing 123/69 = 1
    



