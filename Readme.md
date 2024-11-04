Python tutorials

## Data Types
Integer


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
