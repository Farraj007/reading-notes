[Main Page](../README.md)

# Reading Notes 07  

## Articles  
### Python Scope & the LEGB Rule: Resolving Names in Your Code

[Python Scope](https://realpython.com/python-scope-legb-rule/)  

Understanding Scope  
- Global Scope: The names that you define in this scope are available to all your code.  
- Local Scope: The names that you define in this scope are only available or visible to the code within the scope.  

Using Scope Related Built-In Functions  
- `global()`: is a built-in function that returns a reference to the current global scope or namespace dictionary.  
    - This means if you call `global()` it will return a dictionary of all currently available global variables.  
- `locals()`: is a built-in function that updates and returns a dictionary that holds a copy of the current state of the local python scope or namespace.  
    - THis means if you call `locals()` in a function block, you get all the names assigned in the local scope up to the point where you called `locals()`.  

