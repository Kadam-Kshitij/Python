Python tutorials

## ---- Functions ----
Following error occurs when a function is called too many times. Default Value is 1000
RecursionError: maximum recursion depth exceeded in comparison
We can increase the limit

```
import sys
sys.setrecursionlimit( 2000 )
```

We can access and use a global variable in a function without declaring it as global if you’re only reading its value.

If you try to assign a value to the variable (e.g., message = "New message") without using global, Python will treat it as a local variable, and the global variable will remain unchanged.
