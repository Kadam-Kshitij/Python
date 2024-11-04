Python tutorials

## Data Types
Integer : 23,-10<br/>
Float : 2.3, -0.98<br/>
Complex : 2+3j<br/>
String : "Hello World!"<br/>
List : [ 1, 4, "apple", 4.5]<br/>
Tuple : ( 2, 5, "mango", 9.0 )<br/>
Dictionary : { "key1": "val1", "key2", 56 }<br/>
Set : { 2, 8, 9 }<br/>
Frozen Set : { 2, 4, 9 }<br/>
Boolean : True, False<br/>
None : None<br/>

### List
Ordered - Maintains an order of items and can be accessed by indexing
Mutable - Contents of list can be changed
Can contain different data types

### Tuple
Ordered - Maintains an order of items and can be accessed by indexing
Immutable - Ones created, tuple cannot be modified
Can contain different data types

List can contain tuple. We can add, remove, modify tuples but we cannot change the tuple itself.
Tuple can contain lists. We can modify the list but we cannot change the structure of tuple ( replace the list with other element ).

### Set
UnOrdered - Order of elements is not fixed
Contains Unique elements only. Adding dupicate element causes no change in set.
Can change the contents of set
Can contain tuples, but cannot contain lists. ie. Cannot contain mutable objects

### Frozen Set
Same as set, but cannot be modified ones created.

## Functions
Following error occurs when a function is called too many times. Default Value is 1000
RecursionError: maximum recursion depth exceeded in comparison
We can increase the limit


```
import sys
sys.setrecursionlimit( 2000 )
```

We can access and use a global variable in a function without declaring it as global if we are only reading its value.

If we try to assign a value to the variable without using global, Python will treat it as a local variable, and the global variable will remain unchanged.

By using ```global var``` the global variable will be considered in the function
