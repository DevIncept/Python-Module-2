# **Errors And Exceptions in Python**

In this we are going to discuss about the error and exceptions in Python.</br>

When we develop a program for some task,generation of Errors and Exceptions is obvious .
A programmer needs to find these errors and try to fix them until the program become error free.
This process is called **debugging**.</br>

</br>Errors are the problems in a program due to which the program will stop the execution. On the other hand, Exceptions are basically the error that is  raised after passing the syntax text during the runtime  of the program. 


Normally , A Python program terminates as soon as it encounters an error.</br>
Error in Python can be of two types i.e.</br> - ***Syntax errors*** </br> - ***Logical Error*** (*Exceptions*)

Let Us discuss the both of them in details in below .
1
## **Syntax Error**

Basically the name Syntax Error says it all .This is the error caused for writing the wrong syntax .It normally happens when we start learning new language like Python,C++,C,etc...</br>
For example ,
```Python
>>> i=5
>>> if i == 5 print(i)
  File "<stdin>", line 1
    if i == 5 print(i)
              ^
SyntaxError: invalid syntax
>>>
```
In the above code  we have missed the ‘:’ before the keyword print so it shows syntaxerror.

Common Python Syntax errors include:

- leaving out a keyword
- putting a keyword in the wrong place
- leaving out a symbol, such as a colon, comma or brackets
- misspelling a keyword
- incorrect indentation
- empty block


 
Above , We have learnt about the Syntax Error in Python now lets learn about the exceptions in Python.
## **What Is Exception ?**

As in Introduction , We discussed that **Exception** are the error that occurs at the execution [*Run-time*] of the program .
Eventhough a statement is syntactically correct, it may still cause an error when executed .</br>In general we can say when a program encounters a problem  which it cannot deal with, it raises an exception. It does not stop the execution of the program but it changes the normal flow of the program.

Let It understand by example 
```Python
>>> print(100/0)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
>>>
```

In the above example , 
Python throws the **ZeroDivisionError** Exception .The Exception raised as we are trying to divide the number i.e. 100 in my case by 0.

Let take another example 

```Python
>>> a = 'devincept'
>>> b = 12
>>> print (a + b)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only concatenate str (not "int") to str
>>>
```
In the above example , 
Python throws the **TypeError** Exception .The Exception raised as we are trying to concatenate int to str



### **Python Built-In Exceptions** :
There are several built-in exceptions in Python that are raised when corresponding error occurs .Some Of them are  :-
- ModuleNotFoundError
- ImportError
- MemoryError
- OSError
- SystemError
- ... And so on
  
We can check all the inbuilt exceptions using the built-in *local()* function as follows:

```Python
print(dir(locals()['__builtins__']))
```


***locals()['__builtins__']***
will return a module of built-in exceptions, functions, and attributes. ***dir*** allows us to list these attributes as strings.

```Python

>>> print(dir(locals()['__builtins__']))
['ArithmeticError', 'AssertionError', 'AttributeError', 'BaseException', 'BlockingIOError', 'BrokenPipeError', 'BufferError', 'BytesWarning', 'ChildProcessError', 'ConnectionAbortedError', 'ConnectionError', 'ConnectionRefusedError', 'ConnectionResetError', 'DeprecationWarning', 'EOFError', 'Ellipsis', 'EnvironmentError', 'Exception', 'False', 'FileExistsError', 'FileNotFoundError', 'FloatingPointError', 'FutureWarning', 'GeneratorExit', 'IOError', 'ImportError', 'ImportWarning', 'IndentationError', 'IndexError', 'InterruptedError', 'IsADirectoryError', 'KeyError', 'KeyboardInterrupt', 'LookupError', 'MemoryError', 'ModuleNotFoundError', 'NameError', 'None', 'NotADirectoryError', 'NotImplemented', 'NotImplementedError', 'OSError', 'OverflowError', 'PendingDeprecationWarning', 'PermissionError', 'ProcessLookupError', 'RecursionError', 'ReferenceError', 'ResourceWarning', 'RuntimeError', 'RuntimeWarning', 'StopAsyncIteration', 'StopIteration', 'SyntaxError', 'SyntaxWarning', 'SystemError', 'SystemExit', 'TabError', 'TimeoutError', 'True', 'TypeError', 'UnboundLocalError', 'UnicodeDecodeError', 'UnicodeEncodeError', 'UnicodeError', 'UnicodeTranslateError', 'UnicodeWarning', 'UserWarning', 'ValueError', 'Warning', 'WindowsError', 'ZeroDivisionError', '__build_class__', '__debug__', '__doc__', '__import__', '__loader__', '__name__', '__package__', '__spec__', 'abs', 'all', 'any', 'ascii', 'bin', 'bool', 'breakpoint', 'bytearray', 'bytes', 'callable', 'chr', 'classmethod', 'compile', 'complex', 'copyright', 'credits', 'delattr', 'dict', 'dir', 'divmod', 'enumerate', 'eval', 'exec', 'exit', 'filter', 'float', 'format', 'frozenset', 'getattr', 'globals', 'hasattr', 'hash', 'help', 'hex', 'id', 'input', 'int', 'isinstance', 'issubclass', 'iter', 'len', 'license', 'list', 'locals', 'map', 'max', 'memoryview', 'min', 'next', 'object', 'oct', 'open', 'ord', 'pow', 'print', 'property', 'quit', 'range', 'repr', 'reversed', 'round', 'set', 'setattr', 'slice', 'sorted', 'staticmethod', 'str', 'sum', 'super', 'tuple', 'type', 'vars', 'zip']
>>>
```


### **Exception Handling In Python**

We have seen the many built in function in the above section .
Now , in this we will see how we can handle this exceptions .

Lets take an instance ,</br>

We know that when a program encounters an Exception , then our program terminates with a default error message and most of the time we may want to show the custom message or run a different set of code rather than showing the default error message .

This is said to be **Exception Handling** . Basically It is the process of responding the exceptions in a custom way during the execution of the program .

In Python We Use try-except block to handle exception

## **The try-expect statement**

If the Python program contains code that may raise the exception, we must place that code in the try block. The try block must be followed with the except statement, which contains a block of code that will be executed if there is some exception in the try block.

**Syntax**:-
```Python
# other code
try:    
    #block of code     
    
except ExceptionName:    
    #block of code    
      
#other code    
```

Now, let’s take a look at an example to better understand how an exception is handled in a program.
#### **Code**
```Python
try:  
    a = int(input("Enter a:"))    
    b = int(input("Enter b:"))    
    c = a/b  
except:  
    print("Can't divide with zero")  
```

#### **Output**

```Python
Enter a:10
Enter b:0
Can't divide with zero
```

In the above code first try code is being executed and then if an exception happpened then the except block code is being executed.


## **Multiple Except Blocks**

### **Multiple Except Statements**


In Python , You can have multiple except blocks for a single try statement.A try block can have more than one except block to specify handlers for different exceptions.  The statement that  matches with the exception generated the code inside it will get executed. However, only one handler will be executed. Exception handlers only handle exceptions that occur in the corresponding try block. The syntax for specifying multiple except blocks for a single try block is :


**Syntax**:-
```Python
# other code
try:    
    #block of code     
    
except ExceptionName1:    
    #block of code 
except ExceptionName2:    
    #block of code    

#other code    
```
Now, let’s take a look at an example to better understand it
#### **Code**
```Python
try:  
    a = int(input("Enter number a:"))    
    print(a**2)   
      
except (KeyboardInterrupt):  
    print("You should enter the number")

except (ValueError):
    print("Please Check the datatype before you enter")
```

#### **Output**

```Python
Enter number a:xyz
Please Check the datatype before you enter
```

In the above code first try code is being executed we have taken the input as 'xyz' and then there is  exception happpened i.e. ValueError as the datatype is being wrong as we have to give input an interger value wherea as we have enterned string datatype so the ValueError block code is being executed and output is being showed.



### **Multiple Exception In single Except Block**

In python ,You can also use the same except statement to handle multiple exceptions as follows −


**Syntax**:-
```Python
# other code
try:    
    #block of code     
    
except (<ExceptionName1>,<ExceptionName2>):    
    #block of code   
      
#other code    
```

Now, let’s take a look at an example to better understand how an exception is handled in a program.
#### **Code**
```Python
try :
	a = 3
	if a < 4 :
		b = a/(a-3)
	
	print ("Value of b = ", b)
except(ZeroDivisionError, NameError):
	print ("Error Occurred and Handled")
 
```

#### **Output**

```Python
Error Occurred and Handled
```

In the above code first try code is being executed and then the except block code is being executed as the exception occured is ZerodivisionError.

### **The Else Clause**

In Python, using the else statement, you can instruct a program to execute a certain block of code  that you want in the absence of exceptions.

**Syntax**:-
```Python
# other code
try:    
    #block of code     
    
except ExceptionName:    
    #block of code    
else:
    #block of code

#other code    
```
Now, let’s take a look at an example to better it
#### **Code**
```Python
try:  
    a = int(input("Enter a:"))    
    b = int(input("Enter b:"))    
    c = a/b  
except:  
    print("Can't divide with zero")

else:
    print(c)  
```

#### **Output**

```Python
Enter a:10
Enter b:5
2.0
```

In the above code first try code is being executed and then there is no exception happpened so the else block code is being executed and output is being showed.

### **The Finally Clause**

You can use a finally: block along with a try: block. In Python  finally keyword is the keyword that is executed always irrespective of whether an exception has occured or not after try and except blocks.


**Syntax**:-
```Python
# other code
try:
       # Some Code.... 

except:
       # optional block
       # Handling of exception (if required)

else:
       # execute if no exception

finally:
      # Some code .....(always executed)   
```

Now, let’s take a look at an example to better understand it
#### **Code**
```Python
try:
	k = 5//0 
	print(k)	
except ZeroDivisionError:
	print("Cannot divide by zero")
	
finally:
	print('This is always executed')

```

#### **Output**

```Python
Cannot divide by zero
This is always executed
```

In the above code first try code is being executed and then an exception happpened then the except block code is being executed and then the finally block is being executed.

## **Raising Exceptions**

You can also raise exception by using the raise clause in Python.This comes into picture when we need to raise an exception to stop the execution of program.

To raise an exception , you must use exception class name followed by raise statement.
You can also give value to the exception in the parenthesis.
You can access the value by using "as" keyword.
"e" keyword is used as an reference variable which stores the value of the exception.

**Syntax**:-
```Python
raise Exception_class,<value>      
```


Now, let’s take a look at an example to better understand it

#### **Code:-**
```Python

try:
	raise NameError("Hi there") # Raise Error
except NameError:
	print ("An exception")
	raise # To determine whether the exception was raised or not

```


The output of the above code will simply line printed as “An exception” but a Runtime error will also occur in the last due to raise statement in the last line. So, the output on your command line will look like :-
#### **Output**

```Python
Traceback (most recent call last):  
  File "c:/Users/dwibe/Desktop/devincept/Error And Exceptions/abc.py", line 3, in <module>    
    raise NameError("Hi there") # Raise Error
NameError: Hi there
```


## **Conclusion**
Hopefully, this article helped you understand the Error and Exceptions In Python tand how to  deal with these  exceptions i.e. Exception Handling.
