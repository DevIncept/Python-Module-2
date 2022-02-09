# **List in Python**

## What is a List?

* A List is used to store the sequence of various types of data.

* Data are inclosed inside [ ] brackets seprated by commas(,).

* Lists are mutable in nature it means data which can be changed when required.

* Duplicate entries are allowed in list.

* A list can also have another list as an item. This is called a nested list.


## Syntax:-

    list1 = [ ]           #Empty List
    list2 = [ sequence1 ]
    list3 = [ sequence1, sequence2, sequence3 ]

## Example:-

    language = ['C','C++','Java','Python']       //List of Strings
    number = [3,5,4,9]                           //List of Numbers
    mixed = ['Mango','Apple',1,'Banana',8]       //List of Mixed Data Type 
    nested = [['Raman', 'Nikhil'],[2,5,7]]       //List of Nested List
    deep_nested = ['Honey','Deepak',[1,5,8,['Akshay','Shubham',['India','Australia]]]]              //Deeply Nested

## List index
* Each element in the list has a position in the list known as an index. The list index starts from zero.

|Element   | Index |
| -------- | ----- |
| 23461    | 0     |
| 77149    | 1     |
| 10295    | 2     |
| 14920    | 3     |

* Index positions actually help us to directly access a value from the list. list_name[index] can be used to directly access the list element at the mentioned index position.
* If we want to access an element directly, we can also use it to directly modify an element in the list. element[1] = 23413

## Basic Operations of List


| Python Expression	            |  Result	       |  Operation                           |
| ----------------------------- | ---------------- | ------------------------------------ |
|  [1,2,3]+[8,9,9]	            |  [1,2,3,8,9,9]   |  Concatination                       |
|  len([4,5,6])		            |  3               |  Length                              |
|  7 in [1,4,7]	                |  True	           |  Membership                          |
|  for n in [1,3,5]: print (n)	|  1 3 5	       |  Iteration                           |
|  n=[1,3,7] print(n[2])	    |  7	           |  Indexing: Offset Starts at 0        |
|  n=[1,3,7] print(n[-2])	    |  3	           |  Negative Slicing: Count from right  |
|  n=[1,3,7] print(n[1:])   	|  [3,7]	       |  Slicing                             |

## Built-in methods and functions in lists

|  Function	            |  Description                                                    |
|-----------------------|-----------------------------------------------------------------|
| cmp(list1,list2)	    |  Compare elements of both list                                  |
| len(list)	            |  Give total Length of list                                      |
| max(list)	            |  Return item from list with maximum value                       |
| min(list)	            |  Return item form list with minimum value                       |
| list(seq)	            |  converts a tuple to list                                       |
| list.append(obj)	    |  Append object obj to list                                      |
| list.count(obj)	    |  Return count of how many times obj occurs in list              |
| list.insert(index,obj)|  Insert object obj to list at offset index                      |
| obj=list.pop()	    |  Remove the item at position -1 from list and assigns it to obj |
| list.remove(obj)	    |  Removes object obj from list                                   |
| list.reverse()	    |  Reverses the order of items in list                            |
| sorted(list)	        |  Sorts item in list                                             |

### Example
* cmp(list)

    - This function takes 2 lists as input and checks if the first argument list is greater, equal or smaller than the second argument list.

    - Returns : This function returns 1, if first list is “greater” than second list, -1 if first list is smaller than the second list else it returns 0 if both the lists are equal.    

##
    initializing argument lists
    list1 = [ 1, 2, 4, 3]
    list2 = [ 1, 2, 5, 8]
    list3 = [ 1, 2, 5, 8, 10]
    list4 = [ 1, 2, 4, 3]
    Comparing lists
    print "Comparison of list2 with list1 : ",
    print cmp(list2, list1)
    prints -1,  because list3 has larger size than list2
    print "Comparison of list2 with list3(larger size) : ",
    print cmp(list2, list3)
    prints 0 as list1 and list4 are equal
    print "Comparison of list4 with list1(equal) : ",
    print cmp(list4, list1)

* len(list)
    - Python list method len() returns the number of elements in the list.
##
    list1, list2 = [123, 'xyz', 'zara'], [456, 'abc']
    print "First list length : ", len(list1)
    print "Second list length : ", len(list2)

* max(list) or min(list)
    - Python list method max or min returns the elements from the list with maximum or minimum value.
##
    list1, list2 = [123, 'xyz', 'zara', 'abc'], [456, 700, 200]
    print "Max value element : ", max(list1)
    print "Min value element : ", min(list2)

* list(tuple)
    - The list() method takes sequence types and converts them to lists. This is used to convert a given tuple into list.
##
    aTuple = (123, 'C++', 'Java', 'Python')
    list1 = list(aTuple)
    print ("List elements : ", list1)
* list.append(obj)
    - Python list method append() appends a passed obj into the existing list.
##
    aList = [123, 'xyz', 'zara', 'abc'];
    aList.append( 2009 );
    print "Updated List : ", aList
* list.count(obj)
    - Python list method count() returns count of how many times obj occurs in list.
## 
    aList = [123, 'xyz', 'zara', 'abc', 123];
    print "Count for 123 : ", aList.count(123)
    print "Count for zara : ", aList.count('zara')
* list.insert(index,obj)
    - Python list method insert() inserts object obj into list at offset index.
    - index − This is the Index where the object obj need to be inserted.
    - obj − This is the Object to be inserted into the given list.
##
    aList = [123, 'xyz', 'zara', 'abc']
    aList.insert( 3, 2009)
    print "Final List : ", aList

* list.pop()
    - Python list method pop() removes and returns last object or obj from the list.
##
    aList = [123, 'xyz', 'zara', 'abc'];
    print "A List : ", aList.pop()
    print "B List : ", aList.pop(2)
* list.remove(obj)
    - Python list method remove() searches for the given element in the list and removes the first matching element.
##
    aList = [123, 'xyz', 'zara', 'abc', 'xyz'];
    aList.remove('xyz');
    print "List : ", aList
    aList.remove('abc');
    print "List : ", aList
* list.reverse()
    - Python list method reverse() reverses objects of list in place.
## 
    aList = [123, 'xyz', 'zara', 'abc', 'xyz'];
    aList.reverse();
    print "List : ", aList
* sort(list)
    - The sort() method sorts the list ascending by default.
## 
    cars = ['Ford', 'BMW', 'Volvo']
    cars.sort()