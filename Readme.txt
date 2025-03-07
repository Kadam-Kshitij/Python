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





# Printing to the console
myInt = 2
myFloat = float( 2 ) 	# or 2.0
mystr = "Hello World"
print( "%d %f %s" % ( myInt , myFloat, mystr ) )

# Taking inputs number and string
myI = int( input( "Enter a number : ") )
print( myI )
myS = input( "Enter a String : " )
print( myS )

# Functions in Python
def foo( a, b ):
	print( "A , B = %d , %d " % ( a, b ) )

foo( 23, 45 )

for i in range( 1 , 5 ):
	print( "%d" % i )

a = 5;
while a > 1:
	print( "%d" % a )
	a -= 1
else:
	print( "While else" )


# Dictionary - Unordered key, value pair. Keys are unique
myDictionary = { "John": 23, "Alesx": 33 }
myDictionary["Pika"] = 32
# myDictionary.keys(), myDictionary.values()
for key, value in myDictionary.items():
	print( "%s, %d" % ( key, value ) )
myDictionary.pop( "Alesx" )
print( myDictionary )

# List - Ordered colletion of items of different data types
myList = [34, "aslk", 33.4, "pop"]
for i in range( 0, len(myList) ):
	print( myList[i] )
myList.append(100)
myList.insert( 2, 200 )
print( myList )
myList.pop(3)
print( myList )
subMyList = myList[1:3]
print( subMyList )

# Tuples - Ordered collection of items which cannot be modified ones created
myTuple = (2, 22.3, "lkad" )
for i in range( 0, len(myTuple)):
	print( myTuple[i] )
subMyTuple = myTuple[0:1]
print( subMyTuple )

# Set - UnOrdered colletion of unique elments
mySet = { 2, "askals", 55.5 }
mySet.add( "Pop" )
print( mySet )
mySet.discard( 2 )	# Does nothing if element not present
print( mySet )



class Base:
	def __init__( self, name ):
		self._name = name


class Derived( Base ):
	def __init__( self, name, rollNum ):
		super().__init__( name )
		self.rollNum = rollNum

	def display( self ):
		print( "%s : %s " % ( self._name, self. rollNum ) )

obj = Derived( "alex", 45 )
obj.display()
obj._name = "Carry"
obj.display()
