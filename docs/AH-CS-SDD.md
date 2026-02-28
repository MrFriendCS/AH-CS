# Software Design and Development

## Notes

All the code examples use Python.

These notes are focused on Advanced Higher Computing Science so some terms may be used differently.

## Objects

An object is the way of representing _something_ in software.  A string, such as "Hello", is an objects, but new objec.  An object will have properties and methods:

* Property - data about the object (a variable)
* Method - something the object can do (a sub-program)

### Declaration

``` python
class Person:
    """Declare a class to define a person."""


    def __init__(self, name="", age=0):
        """Object constructor method.  Automatically called when an object is created."""
        
        # Class properties
        self.__name = name  # Private property
        self.__age = age    # Private property
```

When a sub-routine is called it can have parameters passed to it.  These are known as actual parameters.  They must match the formal parameters in order, number, and data types.

``` python
subroutineName(actualParameter1, actualParameter2, ...)
```


### Properties

A procedure is a type of sub-routine that ***does not*** return a value.  It must be defined before it can be used.

``` python
def square(number):
    """Display the square of number."""
    
    # Calculate result
    squared = number ** 2
    
    print(squared)
```

A procedure can be called from the main program, or from another sub-routine.

``` python
square(2)
```


### Methods

A function is another type of sub-routine that ***does*** return a value.  It must be defined before it can be used.

``` python
def toThePowerOf(number, power):
    """Return a number raised to a power."""
    
    # Calculate result
    value = number ** power
    
    return value
```

A function can be called from the main program, or from another sub-routine.  To use the value returned by the function it can be assigned to a variable or used as the a value in another operation.

__Returned value assigned__

``` python
answer = toThePowerOf(2, 5)

print(answer)
```

__Returned value used__

``` python
answer = 64 - toThePowerOf(2, 5)

print(answer)
```


#### Return multiple values

Functions can return a tuple [term not part of Higher] that contains multiple values, similar to an array.  These values can be assigned to individual variables when returned.

``` python
def myData():
    """Return an integer and a string."""
    
    # Return a tuple
    return 21, "Tom"
```

``` python
# Display returned tuple
print(myData())
```

``` python
# Assign to a tuple
myTuple = myData()

# Display the tuple
print(myTuple)

# Display individual values
print(myTuple[0])
print(myTuple[1])
```

``` python
# Assign directly to variables
age, name = myData()

# Display values
print(age)
print(name)
```


## Predefine functions

### Character to ASCII


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwODE5MTE0ODMsLTE5Mzc3MjEzNTEsLT
M4NTMzNTcxLDE5NzcwODI5MDgsLTYyNDUwMjE2Nyw0MjU0Njg5
NzksLTIwNTQ1ODMxMDEsMjE0MTQ0MTkwNiwyMDkyNjM3NzE3LC
0xODMzNjIxOTYzLC05ODMwMTc5NzksOTU5MjE4MDYyLDE2MTIy
NzAzMzIsNzM5NDgzMjYzLDY5NTQyNTU5OSwtMTMxNDU3NzM4My
wxOTQ0OTgyNjM4LDE4NDc4NTA4NTMsLTk2MDkyMDc2MywtODMy
MDg2NTM5XX0=
-->