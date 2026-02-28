# Software Design and Development

## Notes

All the code examples use Python.

These notes are focused on Advanced Higher Computing Science so some terms may be used differently.

## Objects

An object is the way of representing _something_ in software.  A string, such as "Hello", is an object.  An object will have properties and methods:

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


```


## Predefine functions

### Character to ASCII


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwNTUwMTA1OTYsOTU5NzIyNTk4LC0xOT
M3NzIxMzUxLC0zODUzMzU3MSwxOTc3MDgyOTA4LC02MjQ1MDIx
NjcsNDI1NDY4OTc5LC0yMDU0NTgzMTAxLDIxNDE0NDE5MDYsMj
A5MjYzNzcxNywtMTgzMzYyMTk2MywtOTgzMDE3OTc5LDk1OTIx
ODA2MiwxNjEyMjcwMzMyLDczOTQ4MzI2Myw2OTU0MjU1OTksLT
EzMTQ1NzczODMsMTk0NDk4MjYzOCwxODQ3ODUwODUzLC05NjA5
MjA3NjNdfQ==
-->