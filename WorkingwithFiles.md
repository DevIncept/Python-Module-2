![files](https://user-images.githubusercontent.com/85128689/125448683-4d8d9845-d20a-4898-b2aa-4a84bf24f241.jpeg)
# File handling with Python
-----------------------------------------------
## File:  
- File is a named location on a secondary storage device where data are permanently stored for later access.  

## File Handling:
- The process of creating a file, storing the data in it, retrieving data from it and appending further information is said to be File Handling.

## Does python support file handling:
- Python supports file handling like many other programming languages.
- There are many programming languages that supports file handling, in some languages this topic is a bit complicated, but in python file handling is very easy.

## Use of file handling in Python:
- File handling provies various modes(read mode, write mode etc) to operate a file.
- We can create a new file using python code, open existing files, write in files ,read data from files and many more such options.
## There are mainly two types of data files
- Text file
- Binary file
## Text file
- A text file can be understood as a sequence of characters consisting  of  alphabets,  numbers  and  other  special symbols
- File extensions like .txt, .py, .csv, etc. are few examples of text files.
- Each  line  of  a  text  file  is  stored  as  a  sequence of  ASCII  equivalent  of  the  characters.
- This  is terminated by a special character called the End of Line (EOL).
## Binary file
- Binary  file  consists  of  data  stored  as  a  stream of bytes.
- Binary files are mainly used to store data beyond text such as images, executables, etc.  

## Opening and Closing Files 
Python consists of various built in functions and methods to manipulate files. These functions and methods bascically work on a file object
- **The Open() Function:**
    - Python built in open() function is used to open the file for reading or writing to it.
    - The syntax of **open()** is:
    
    |Syntax||
    |-|-|
    |**fileObj= open(file_name[,access_mode])**||  
    - Here,
        - file_name is string value that specifies name of the file that you want to access.
        - access_mode indicates the mode in which the file is supposed to be opened i.e., read,write, etc.
- **The Close() Function:**
    - The close() method is used to close the file object.
    - Once a file object is closed, you cannot further read from or write into the file that is associated with this file object.
    - The Syntax of **close()** is:  
    |Syntax:|
    |-|
    |fileobj.close()|
    
## Access Modes in Python
  
|Modes|Purpose|
|-|-|
|r|Opens the file in read-only mode|
|rb|Opens the file in read-only binary format mode|
|r+|Opens the file in both read and write mode|
|rb+|Opens the file in both read and write mode in binary format|
|w|Opens the file in write mode. If the file doesn't exists then a new file will be created.|
|wb|Opens the file in write mode for binary format only|
|w+|Opens the file in both read and write mode. If the file doesn't exist, a new file is created for reading as well as writing.If the file already exists then contents are overwritten|
|wb+|Opens the file in both read and write for binary format only.If the file doesn't exist, a new file is created for reading as well as writing.If the file already exists then contents are overwritten|
|a|Opens a file for appending.The pointer is placed at the end of the file if the file exists. If file doesn't exist, it creates a new file for writing.|
|ab|Opens a file in binary format for appending.The pointer is placed at the end of the file if the file exists. If file doesn't exist, it creates a new file for writing.|
|a+|Opens a file for both reading and appending.The pointer is placed at the end of the file if the file exists. If file doesn't exist, it creates a new file for reading and writing.|
|ab+|Opens a file in binary for both reading and appending.The pointer is placed at the end of the file if the file exists. If file doesn't exist, it creates a new file for reading and writing.|  

If no mode is specified then 'r' is considered as default mode.


## The File Object Attributes

|Attribute|Information Obtained|
|-|-|
|file.mode|it returns the access mode in which file is opened|
|file.name|it returns the name of the file|
|file.close|it is used to close the file|
|file.closed|it returns True if file is closed,False if not.|
|read([size])|It reads the specified number of bytes(the size specified) from the file.|
|readline([size])|It is used to read one entire line from a file|
|tell()|This returns the current position of file pointer.|
|write(str)|This writes a string into the file.|
|writelines(sequence)|This writes a sequence of strings into the file|


## Examples


```python
file = open("devincept.txt", "r") 
print (file.read())
```

    DevIncept 
    Learn by Developing!
    


```python
file = open('a.txt','w')
file.write("I want do an Internship ")
file.close()
```


```python
file = open('a.txt','a')
file.write("\nI Love DevIncept")
file.close()
```


```python
file=open("a.txt",'r')
print(file.read())
```

    This is words motivates me
    I Love DevIncept
    


```python
f = open('story.txt', 'r') 
text = f.read(53)  
print(text) 
f.close() 
```

    Once upon a time, in a field not too far from you, th
    


```python
f = open('story.txt','r')
text = f.readline(20) 
print(text) 
f.close() 
```

    Once upon a time, in
    


```python
f = open('story.txt', 'r') 
text = f.readlines(25) 
print(text) 
f.close() 
```

    ['Once upon a time, in a field not too far from you, there was an energetic and happy hare and a sleepy tortoise.\n']
    


```python
f = open('B.txt','w+') 
lines = "It's a new day\n"
f.write(lines) 
f.close() 
```


```python
f = open('C.txt', 'a+') 
lines = "New day!"
f.write(lines) 
f.close() 

```


```python
file=open("devincept.txt","wb")
print("Name of the file:",file.name)
print("File is closed",file.closed)
print("File has been opened in",file.mode,"mode")
```

    Name of the file: devincept.txt
    File is closed False
    File has been opened in wb mode
    
![Tqq](https://user-images.githubusercontent.com/85128689/123909514-c9dda500-d996-11eb-8808-f2156178daac.jpeg)
