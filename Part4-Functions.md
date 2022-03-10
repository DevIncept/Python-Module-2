**FUNCTIONS IN PYTHON**:smiley: :smiley:



-**What is function ** :question:

    A function is a block of code that performs a task. 
    It can be called and reused multiple times. 
    You can pass information to a function and it can send information back. 
    Many programming languages have built-in functions that you can access in their library, but you can also create your own functions.

    When you call a function, the program will pause the current program and execute the function. 
    The function will be read from top to bottom. Once the function is complete, The program continues to run where it had paused. 
    If the function returned a value, that value will be used where the function was called.


-**Types of function**

      Built in function(len(),type(),input())
      
      Function in module(sin(),cos(),sqrt())
      
      User define function
      
-**How to use builtin function** :question:

      Built-in Functions:

     Built-in functions are part of Python language.These are the functions readily available for the use.

     Examples
    Function	Description
    max()	Returns the largest item in an iterable
    min()	Returns the smallest item in an iterable
    input()	To accept the input from the user
    
    
-**How to use functions of module **:question:
 
    It can be used by just importing the module then you can use same as built in function.
    # import the math module 
    import math 
  
    # print the square root of  0 
    print(math.sqrt(0)) 
  
    # print the square root of 4
    print(math.sqrt(4)) 
    
    
-**How to define a function ** :question: 

    The keyword def introduces a function definition. It must be followed by the function name and the parenthesized list of formal parameters.
    The statements that form the body of the function start at the next line, and must be indented.
       *FUCTION HEADER that begin with def and ends with ":"
       *PARAMETERS variables that are listed within parenthesis
       *FUNCTION BODY block of statements/indented-statements beneath function header that defines the action performed by the function.
       *IDENTATION 
    
    def - to declare/define the function
    function-name- name of the function
    () - required to distinguish between a variable and function and end the definition with a semi-colon
    example:
    def helloFunction():
      print("Hello World")
      
    helloFunction()
  
-**RETURN TYPE FUNCTION**

    fuctions that return value.
    A return statement is used to end the execution of the function call and “returns” the result (value of the expression following the return keyword) to the caller. 
    The statements after the return statements are not executed. 
    If the return statement is without any expression, then the special value None is returned.
    Syntax:

    def fun():
        statements
         .
         .
        return [expression]
      eg:
     # Python program to 
     # demonstrate return statement 
  
    def add(a, b):
  
       # returning sum of a and b
       return a + b
  
    def is_true(a):
  
        # returning boolean of a
        return bool(a)
  
    # calling function
    res = add(2, 3)
    print("Result of add function is {}".format(res))
  
    res = is_true(2<5)
    print("\nResult of is_true function is {}".format(res))
    
    
           
        
