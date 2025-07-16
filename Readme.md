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
Ordered - Maintains an order of items and can be accessed by indexing<br/>
Mutable - Contents of list can be changed<br/>
Can contain different data types<br/>

### Tuple
Ordered - Maintains an order of items and can be accessed by indexing<br/>
Immutable - Ones created, tuple cannot be modified<br/>
Can contain different data types<br/>

List can contain tuple. We can add, remove, modify tuples but we cannot change the tuple itself.<br/>
Tuple can contain lists. We can modify the list but we cannot change the structure of tuple ( replace the list with other element ).<br/>

### Set
UnOrdered - Order of elements is not fixed<br/>
Contains Unique elements only. Adding dupicate element causes no change in set.<br/>
Can change the contents of set<br/>
Can contain tuples, but cannot contain lists. ie. Cannot contain mutable objects<br/>

### Frozen Set
Same as set, but cannot be modified ones created.<br/>

## Functions
Following error occurs when a function is called too many times. Default Value is 1000<br/>
RecursionError: maximum recursion depth exceeded in comparison<br/>
We can increase the limit<br/>

```
import sys
sys.setrecursionlimit( 2000 )
```

We can access and use a global variable in a function without declaring it as global if we are only reading its value.<br/>

If we try to assign a value to the variable without using global, Python will treat it as a local variable, and the global variable will remain unchanged.<br/>

By using ```global var``` the global variable will be considered in the function<br/>


# Printing to the console
```
myInt = 2
myFloat = float( 2 ) 	# or 2.0
mystr = "Hello World"
print( "%d %f %s" % ( myInt , myFloat, mystr ) )
```

# Taking inputs number and string
```
myI = int( input( "Enter a number : ") )
print( myI )
myS = input( "Enter a String : " )
print( myS )
```

# Functions in Python
```
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
```


# Dictionary - Unordered key, value pair. Keys are unique
```
myDictionary = { "John": 23, "Alesx": 33 }<br/>
myDictionary["Pika"] = 32
# myDictionary.keys(), myDictionary.values()
for key, value in myDictionary.items():
	print( "%s, %d" % ( key, value ) )
myDictionary.pop( "Alesx" )
print( myDictionary )
```

# List - Ordered colletion of items of different data types
```
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
```

# Tuples - Ordered collection of items which cannot be modified ones created
```
myTuple = (2, 22.3, "lkad" )
for i in range( 0, len(myTuple)):
	print( myTuple[i] )
subMyTuple = myTuple[0:1]
print( subMyTuple )
```

# Set - UnOrdered colletion of unique elments
```
mySet = { 2, "askals", 55.5 }
mySet.add( "Pop" )
print( mySet )
mySet.discard( 2 )	# Does nothing if element not present
print( mySet )
```

# Class
```
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
```

# Casting
```
i = int( "3" )
f = float( "3.4" )
s = str( 4 )

print( "%d, %f, %s" % ( i, f, s ) )		# 3, 3.400000, 4
```

# String
```
str = "Hello how are you ?"

print( str[2] ) # l

for i in str:
	print( i )	# Prints one letter at a time. Each on a new line

if "how" in str:
	print( "True" )		# True
else:
	print( "False" )

strMulti = """ How are you
This is a multi 'line' statement"""
print( strMulti )
```

# if else
```
a = -80
if a > 0:
	print( "Greater" )
elif a == 0:
	print( "Equal" )
else:
	print( "Lower" )	# Lower

b = 90
if a < 0 and b > 0:
	print( "aandb" )	# aandb

if a > 0 or b > 0:
	print( "aorb" )	# aorb

if not a > 0:
	print( "nota" )	#nota
```

# While
```
a = 1

while a < 10:	# while
	if a%2 == 0:
		a += 1
		continue	# continue
	print( a )
	a += 1
else:	# Executed ones when while loop ends
	print( "Done" )
# Else not executed in case of break happens
```

# For
```
for i in range( 1, 11, 2 ):
	print( i )
# Prints 1, 3, 5, 7, 9
# Starts from 1 to 11 ( 11 not included ) with a increment step of 2
# continue, break, else statemets can be used just like while
```

# Functions
```
def func(*para):
	print( para[2] )

func( 90, 91, 92, 93 )	# 92
# Error in case function call does not have

def foo(p1, p2, p3):
	print( p1, p2, p3)
foo(p3 = 90, p1 = 91, p2 = 92)	# 91, 92, 90

def goo(p1 = 80):
	print( p1 )
goo()	# 80
```

# Lambda
```
a = lambda x, y, z : x + y + z
print( a( 9, 8, 7 ) )	# 24
```

# Class
```
class Base:
	def __init__( self, a, b ):
		self.a = a
		self.b = b

	def __str__( self ):
		return str(self.a) + ", " + str(self.b)

	def print( self ):
		print( self.a, self.b )

obj = Base( 90, 80 )	
print( obj ) 	# 90, 80
obj.print()		# 90 80

del obj.a
# obj.print()	# Error - Base object has no attribute a

del obj
# obj.print()	# Error - obj not defined
```

# Inheritance
```
class Base1:
	def __init__( self, a ):
		self.a = a

class Base2:
	def __init__( self, a ):
		self.b = a

	def printVal( self ):
		print( self.b )

class Derived:
	def __init__( self, a, b ):
		Base1.__init__( self, a )
		Base2.__init__( self, b )

	def printVal( self ):
		print( self.a, self.b )	# 90 80
		Base2.printVal( self )	# 80 

obj = Derived( 90, 80 )
obj.printVal()
```

# Try Except
```
try:
	print( x )
except NameError:	# Catch name error
	print( "Name error" )
except:				# Catch other errors
	print( "Error occured" )
else:	# Executed if error does not occur
	print( "Else" )
finally:
	print( "Done" )
```

# Fibonacci
```
def fibo():
	a = 1
	b = 1
	for i in range(10):
		temp = a
		a = b
		b = temp + b
		yield b


for i in fibo():
	print( i )
```
