![h](https://github.com/Scripturient101/Intern-Work/blob/main/Int-py-11/Images/Article_banner.png)

## Objective
Learn about modules in Python and their uses.

## Background
To simplify programming and to logically organize your code, small handleable units called modules are created.

## Table of Contents
- [Overview](#about)
- [Steps to Create and Import a Module ](#steps)
   - Creating a Module
   - Importing a Module
- [Other Ways to Use Import](#ways)
   - [Import with Renaming](#renaming)
   - [Import using from](#from)
   - [Import using from *modulename* import*](#import*)
- [Types of Modules](#types)
   - [Built-in Modules](#builtin)
   - [User-defined Modules](#user-defined)
   - [Third-party Modules](#third-party)
- [The help() function](#help)
- [The dir() function](#dir)


<br>

## Overview <a name="about"></a>

**Module** helps us to arrange our Python code logically. The code is easier to comprehend and use when it is organized into modules. A module is a Python file that contains a collection of **functions** and **variables** that may be used in a program. Any sort of variable can be used (arrays, dictionaries, objects, etc.)
   
## Steps to Create and Import a Module<a name="steps"></a> 
-  Create a new file.
- Name the file and add `.py` extention at the end (i.e. yourfileName.py)
- Declare variables and create functions.

     **Try this example:**<br>
       Create a file named `greetingLearners.py`

     ```python
     def welcome(name):
      print("Hi "  +name,"! Welcome to DevIncept")

     def address(addr):
      print("Your Address is: "  +addr)
     ```

     :clipboard: Note: The module `greetingLearners.py` is ready to use.
 <br>
 
- Use the module in a another code through import
     <br> Create a file named `mainmod.py`

     ```python
     import greetingLearners
     greetingLearners.welcome("Raj")
     ```
   In the first line, `import greetingLearners`, you import the code in the greeting module and make it available to use. In the second line, you access the welcome function within the greetingLearners module
     >Output: Hi Raj ! Welcome to DevIncept 
   <br>

## Other Ways to Use Import <a name="ways"></a>
 <br />
 
In the above section we have directly used the *import* statement however there are other ways to use it.

 <br />
 
<p align="center"><img src="https://github.com/Scripturient101/Intern-Work/blob/main/Int-py-11/Images/Ways_import.png" width="40%"></p> 

- **Import with renaming:** <a name="renaming"></a><br>
Incase the module name is too big to use repeatedly or you want to give it a more relevant name then you can create an alias, by using the *as* keyword. 

  ```python
  import greetingLearners as greet
  greet.welcome("Raj")
  ```
  > Output: Hi Raj ! Welcome to DevIncept
 
   :clipboard: Note: If you use `greetingLearners.welcome("Raj")` in the above code then you will find an error. This is because `greetingLearners` is no longer recognized.
- **Import using from:**<a name="from"></a> <br>
   Only a specific part of a module may be imported using the from keyword. For example, if our module contains many functions and we only need a single function, why would we import the entire module to perform a task that might be performed by a single function specified in that module?

  ```python
  from greetingLearners import address
  address("Delhi")
  ```
  > Output: Your Address is: Delhi
  
  :clipboard: Note: We only imported the `address` function from the `greetingLearners` module, and trying to use any other function would result in an error.
  
- **Import using from modulename import***<a name="import*"></a> <br>
   <br>It can be used if you want to import all functions from the module and do not want to prefix `greetingLearners` while calling them.

    ```python
    from greetingLearners import* 
    welcome("Simran")
    ```
    > Output: Hi Simran ! Welcome to DevIncept

   :clipboard: Note: If used, it becomes difficult to determine what items used in the code are actually coming from the module'. This can create problems ahead.
  
   <br />
   
## Types of Modules <a name="types"></a>
<p align="center"><img src="https://github.com/Scripturient101/Intern-Work/blob/main/Int-py-11/Images/Module_types.png" width="40%"></p> 

- **Built-in** <a name="builtin"></a> </br>
   Python includes many built-in modules. These modules may be used in Python applications by **simply importing them using the keyword 'import' after their name**. Built-in        modules in Python are written in C and integrated with the interpreter.

   Suppose you want to check whether a **particular year is a leap year or not**: if you don't have the support of Python modules, you will have to **perform several operations    such as divide and multiply** to check whether the given year is a leap year or not. But there is a **module in Python that makes this task pretty easy**: simply import that    module and pass the year as an argument in the method, and it will tell you if the given year is a leap year or not.

   Let's illustrate this through a code example:

   ### Without Module:
   ```python
    if (Year % 4) == 0:
        if (Year % 100) == 0:
            if (Year % 400) == 0:
                return True
            else:
                return False
        else:
             return True
    else:
        return False
   ```

   > Output: False
   
   ### With Module: 

   ```python
   import calendar # calendar is a module
   print(calendar.isleap(Year)) # is.leap() is a function define in calendar module
   ```
   > Output: False
   
- **User-defined** <a name="user-defined"></a> </br>
   The user-defined modules is written by the user at the time of program writing.

   Let's illustrate this through a code example:
   Here we are going to create a `.py` file with some code written on that.
   ```python
   def sum(a, b):
      return a+b
   ```
   **Note:** *Give above file name as `sum_num.py`*

   To call this Python module `sum_num.py`, create another Python file `find_sum.py` and use the **import** statement.
   ```python
   import sum_num
   print(sum_num.sum(5, 3))
   ```
   **Note:** *Give above file name as `find_sum.py`*
   > Output: 8

 <br />
 
- **Third-party Modules** <a name="third-party"></a>
   </br>
   Any code written by a third party is called a third-party module. You may use them to make your code more functional, without having to write it yourself, they don’t come in-built with Python and are needed to install.

   Let's see some of them: 
   - **Wikipedia:**
   We now can import the whole Wikipedia! Yes, we can now use the Wikipedia module in Python to import Wikipedia. Use Python to take advantage of the never-ending flood of information.

        ```python
           pip install wikipedia
        ```

        ```python
           import wikipedia
           result = wikipedia.page("Bill Gates")
           print(result.summary)
       ```
   - **Emoji:** 
   Use to create emoji's, For this, emoji module is needed to be installed.

        ```python
           pip install emoji
        ```

        ```python
           from emoji import emojize
           print(emojize(":thumbs_up:"))
        ```
        > Output: 👍
        
     <br />

   ## The help() function <a name="help"></a> </br>
   Use the following command in the Python terminal to see a list of all available modules:
   ```python
   >>> help('modules')
   ```
   Some of the frequently used ones are discussed below:
   | Modules | Description |
   | --------------  | ------------- |
   | Operator | This module contains a set of pre-defined functions that correspond to Python operators. |
   | Decimal  | When one integer is divided by another, this module is used to output the entire decimal value.  |
   | random   | Random numbers are generated with this module. This module's pre-defined functions include randint(), choice(), uniform, and others.   |
   | string    | The string module contains a set of functions for performing various operations on characters. Capwords, ASCII letters, and other functions are pre-defined in this module.   |
   | math    | Mathematical operations are performed using the Math module. This module contains predefined mathematical functions such as sqrt, factorial, and so on.  |


   <br />
   
   ## The dir() function <a name="dir"></a>
   **dir()** produces a sorted list of names specified in the given module. This list covers all of the module's sub-modules, variables, and functions.<br>

   **Case 1:** Without importing external libraries
   ```python
   print(dir())
   ```
         Output: ['__annotations__', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__']
   <br>

   **Case 2:** With importing external libraries
   ```python
   import random
   import operator 
   print(dir())
   ```
         Output: ['__annotations__', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', 'operator', 'random']
   <br>

   ```python
   import random
   print(dir(random))
   ```
         Output: ['BPF', 'LOG4', 'NV_MAGICCONST', 'RECIP_BPF', 'Random', 'SG_MAGICCONST', 'SystemRandom', 'TWOPI', '_Sequence', '_Set', '__all__', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', '_accumulate', '_acos', '_bisect', '_ceil',
         '_cos', '_e', '_exp', '_inst', '_log', '_os', '_pi', '_random', '_repeat', '_sha512', '_sin', '_sqrt', '_test', '_test_generator', '_urandom', '_warn', 'betavariate', 'choice', 'choices', 'expovariate', 'gammavariate', 'gauss', 'getrandbits', 'getstate', 'lognormvariate', 'normalvariate', 'paretovariate', 'randint', 'random', 'randrange', 'sample', 'seed', 'setstate', 'shuffle', 'triangular', 'uniform', 'vonmisesvariate', 'weibullvariate']
