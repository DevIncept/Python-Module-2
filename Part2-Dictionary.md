<h2 align="center"> DICTIONARIES IN PYTHON </h2>
<h3 align="center"> This mark down file helps understand DICTIONARIES  in PYTHON.

### 📋 **DICTIONARIES** 
* Dictionary in Python is an unordered collection of data values, used to store data values like a map, which unlike other Data Types that hold only single value as an element, Dictionary holds ***key:value*** pair. Key value is provided in the dictionary to make it more optimized.


* Each key is separated from its value by a colon **(:)**, the items are separated by commas, and the whole thing is enclosed in curly braces. An empty dictionary without any items is written with just two curly braces, like this: **{}**.


* Keys are ***unique*** within a dictionary while values may not be. The values of a dictionary can be of any type, but the keys must be of an immutable data type such as strings, numbers, or tuples.


```python
# Example
thisdict = {
"Company": "Maruti",
"model": "Swift",
"year": 2020
}
print(thisdict)
# Output:
```

    {'Company': 'Maruti', 'model': 'Swift', 'year': 2020}
    


```python
# Example 2:
dict = {'Name': 'Zara', 'Age': 7, 'Class': 'First'}
print("dict['Name']: ", dict['Name'])
print("dict['Age']: ", dict['Age'])
# Output:
```

    dict['Name']:  Zara
    dict['Age']:  7
    

### 📋 **PROPERTIES OF DICTIONARY**

Dictionary values have no restrictions. They can be any arbitrary Python object, either standard objects or user-defined objects. However, same is not true for the keys. 

There are two important points to remember about dictionary keys:

1. More than one entry per key not allowed. Which means no duplicate key is allowed. When duplicate keys encountered during assignment, the last assignment wins. For example:


```python
thisdict = {
"Company": "Maruti",
"model": "Swift",
"year": 2020,
 "model": "WagonR"   #then the value which is last assigned is considered as the value of the key.
}
print(thisdict)
# Output:
```

    {'Company': 'Maruti', 'model': 'WagonR', 'year': 2020}
    

2. Keys must be immutable. Which means you can use strings, numbers or tuples as dictionary keys but something like ['key'] is not allowed. Following is a simple example:


```python
dict = {['Name']: 'Zara', 'Age': 7}
print("dict['Name']: ", dict['Name'])
# When the above code is executed, it produces the following result which will be an error
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-10-bd5391ecc03c> in <module>()
    ----> 1 dict = {['Name']: 'Zara', 'Age': 7}
          2 print("dict['Name']: ", dict['Name'])
          3 # When the above code is executed, it produces the following result which will be an error
    

    TypeError: unhashable type: 'list'


### 📋 **ACCESSING ITEMS**

- You can access the items of a dictionary by referring to its key name, inside square brackets:


```python
#Example1:
thisdict = {
"Company": "Maruti",
"model": "Swift",
"year": 2020
}
x = thisdict["model"]
print(x)
# Output:
```

    Swift
    


```python
#Example2:
dict = {'Name': 'Zara', 'Age': 7, 'Class': 'First'}
print("dict['Name']: ", dict['Name'])
print("dict['Age']: ", dict['Age'])
# Output:
```

    dict['Name']:  Zara
    dict['Age']:  7
    

#📋  **UPDATING DICTIONARY**
- You can update a dictionary by adding a new entry or a key-value pair, modifying an existing entry, or deleting an existing entry as shown below in the simple example:


```python
# Example:
dict = {'Name': 'Zara', 'Age': 7, 'Class': 'First'}
dict['Age'] = 8; # update existing entry
dict['School'] = "DPS School"; # Add new entry

print("dict['Age']: ", dict['Age'])
print("dict['School']: ", dict['School'])
# Output:
```

    dict['Age']:  8
    dict['School']:  DPS School
    

#📋  **LOOP THROUGH A DICTIONARY**

---



* You can loop through a dictionary by using a for loop.
* When looping through a dictionary, the return value are the keys of the dictionary, but there are methods to return the values as well.




```python
#Example1
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
for x in thisdict.values():
  print(x)

#Output  
```

    Ford
    Mustang
    1964
    


```python
#Example2
## You can also use the values() method to return values of a dictionary:
statesAndCapitals = {
                     'Gujarat' : 'Gandhinagar',
                     'Maharashtra' : 'Mumbai',
                     'Rajasthan' : 'Jaipur',
                     'Bihar' : 'Patna'
                    }
                      
print('List Of given capitals:\n')
  
# Iterating over values
for capital in statesAndCapitals.values():
    print(capital)
#Output   

```

    List Of given capitals:
    
    Gandhinagar
    Mumbai
    Jaipur
    Patna
    


```python
#Example3
#Loop through both keys and values, by using the items() method:
statesAndCapitals = {
                     'Gujarat' : 'Gandhinagar',
                     'Maharashtra' : 'Mumbai',
                     'Rajasthan' : 'Jaipur',
                     'Bihar' : 'Patna'
                    }
                      
print('List Of given states and their capitals:\n')
  
for state, capital in statesAndCapitals.items():
    print(state, ":", capital)
 #Output   
```

    List Of given states and their capitals:
    
    Gujarat : Gandhinagar
    Maharashtra : Mumbai
    Rajasthan : Jaipur
    Bihar : Patna
    

#📋   **DICTIONARY LENGTH**
* To determine how many items (key-value pairs) a dictionary has, use the len() function.


```python
#Example1
dict1 ={'Name':'Steve', 'Age':30, 'Designation':'Programmer'}
  
# using len() counts the
# number of entries
print("len() method :", len(dict1))
#OutPut
```

    len() method : 3
    


```python
#Example2
dict1 ={'Name':'Steve', 'Age':30, 'Designation':'Programmer'}
# using dict.keys() counts
# the no.of.keys in dictionary
print("len() method with keys() :", len(dict1.keys()))
#Output
```

    len() method with keys() : 3
    


```python
#Example3
dict1 ={'Name':'Steve', 'Age':30, 'Designation':'Programmer'}
# using dict.values() counts
# the no.of.valuess in dictionary
print("len() method with values():", len(dict1.values()))
#OutPut

```

    len() method with values(): 3
    

#📋  **ADD NEW KEYS TO A DICTIONARY**


```python
#Method1
dict = {'FirstName':'Rohit', 'LastName':'Sharma'}
print("Current Dict is: ", dict)
# using the subscript notation
# Dictionary_Name[New_Key_Name] = New_Key_Value
dict['FirstName'] = 'Mahendra'
dict['LastName'] = 'Singh Dhoni'
print("Updated Dict is: ", dict)
#Output
```

    Current Dict is:  {'FirstName': 'Rohit', 'LastName': 'Sharma'}
    Updated Dict is:  {'FirstName': 'Mahendra', 'LastName': 'Singh Dhoni'}
    


```python
#Method2
#Using update() method
dict = {'FirstName':'Rohit', 'LastName':'Sharma'}
dict.update({'Gender':'Male'})
print("Updated Dict ",dict)
#Output
```

    Updated Dict  {'FirstName': 'Rohit', 'LastName': 'Sharma', 'Gender': 'Male'}
    


```python
#Method3
#Using __setitem__
dict = {'FirstName':'Rohit', 'LastName':'Sharma'}
dict.__setitem__('Height', "5'9")
print("Updated Dict",dict)
#Output
```

    Updated Dict {'FirstName': 'Rohit', 'LastName': 'Sharma', 'Height': "5'9"}
    

#📋   **REMOVING ITEMS**
* There are several methods to remove items from a dictionary:


```python
#Method1
test_dict = {"Arushi" : 22, "Anuradha" : 21, "Mani" : 21, "Haritha" : 21}
  
# Using del to remove a dict
# removes Mani
del test_dict['Mani']
print(test_dict)
#Output
```

    {'Arushi': 22, 'Anuradha': 21, 'Haritha': 21}
    


```python
#Method2
test_dict = {"Arushi" : 22, "Anuradha" : 21, "Mani" : 21, "Haritha" : 21}
  
# Using pop() to remove a dict. pair
# removes Anuradha
removed_value = test_dict.pop('Anuradha')
print(test_dict)
#Output
```

    {'Arushi': 22, 'Mani': 21, 'Haritha': 21}
    


```python
#Method3
test_dict = {"Arushi" : 22, "Anuradha" : 21, "Mani" : 21, "Haritha" : 21}
  
# Using items() + dict comprehension to remove a dict. pair
# removes Arushi
new_dict = {key:val for key, val in test_dict.items() if key != 'Arushi'}
print(new_dict)
#Output
```

    {'Anuradha': 21, 'Mani': 21, 'Haritha': 21}
    

#📋 **COPY A DICTIONARY**

* They copy() method returns a shallow copy of the dictionary


```python
#Example1
# of dictionary copy
original = {1:'Webdev', 2:'Machine Learning'}
  
# copying using copy() function
new = original.copy()
  
# removing all elements from the list
# Only new list becomes empty as copy()
# does shallow copy.
new.clear() 
  
print('new: ', new)
print('original: ', original)
#Output
```

    new:  {1: 'Webdev', 2: 'Machine Learning'}
    original:  {1: 'Webdev', 2: 'Machine Learning'}
    


```python
#Example2
#Unlike copy(), the assignment operator does deep copy.
original = {1:'Webdev', 2:'Machine Learning'}
  
# copying using copy() function
new = original.copy()
  
# removing all elements from new list
# and printing both
new.clear()
print('new: ', new)
print('original: ', original)
  
original = {1:'andriodDev', 2:'Data Science'}
  
# copying using =
new = original
  
# removing all elements from new list
# and printing both
new.clear()
print('new: ', new)
print('original: ', original)
#Output
```

    new:  {}
    original:  {1: 'Webdev', 2: 'Machine Learning'}
    new:  {}
    original:  {}
    

##📋   **BUILT-IN METHODS OF DICTIONARY**

|Methods|Description|
|-------|-----------|
|clear()|	Removes all items from the dictionary.|
|copy()|	Returns a shallow copy of the dictionary.|
|fromkeys(seq[, v])|	Returns a new dictionary with keys from seq and value equal to v (defaults to None).|
|get(key[,d])|	Returns the value of the key. If the key does not exist, returns d (defaults to None).|
|items()|	Return a new object of the dictionary's items in (key, value) format.|
|keys()|	Returns a new.|
|all()|	Return True if all keys of the dictionary are True (or if the dictionary is empty).|
|any()|	Return True if any key of the dictionary is true. If the dictionary is empty, return False.|
|len()|	Return the length (the number of items) in the dictionary.|
|cmp()|	Compares items of two dictionaries. (Not available in Python 3)|
|sorted()|	Return a new sorted list of keys in the dictionary.|



```python

```
