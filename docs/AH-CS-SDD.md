# Software Design and Development

## Notes

All the code examples use Python.

These notes are focused on Advanced Higher Computing Science so some terms may be used differently.

## Object-Orientated Programming (OOP)

Classes create objects.  Objects have properties and methods.

An object is a way of representing _something_ in software, e.g. a person or a vehicle.  Objects have properties and methods:

* Property - something about the object (a variable: data)
* Method - something the object can do (a sub-program: behaviour)

### Declaration

The `class` keyword is used to declare the _blueprint_ for new objects.  New classes are named using `CapitalisedWords`.

A class contains a constructor method, `__init__`, which is used to create a new object.  It is called automatically when an object is created.

``` python
class Person:
    """Declare a class to define a person."""

    def __init__(self, name="", age=0):
        """Object constructor method.  Automatically called when an object is created."""
        
        # Class properties
        self.__name = name  # Private property
        self.__age = age    # Private property
```

An example of instantiation, creating and object, is shown below:

``` python
# Create a new object
newPerson = Person(("Tom", 18)
```

### Properties

A procedure is a type of sub-routine that ***does not*** return a value.  It must be defined before it can be used.

``` python

```

A procedure can be called from the main program, or from another sub-routine.

``` python
```


### Methods

A function is another type of sub-routine that ***does*** return a value.  It must be defined before it can be used.

``` python
```

A function can be called from the main program, or from another sub-routine.  To use the value returned by the function it can be assigned to a variable or used as the a value in another operation.


## Predefine functions

### Character to ASCII


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4NzczMjc5MDQsLTE0NDg5NTYxMDIsMT
gyNjk5NzE1NiwtNDc1NzMxODIyLDk5NzM3NTYxOSwtMTkzMjg0
ODc5LC0xNDE4NTk5NjgsLTEwODkxMzYzNzMsOTU5NzIyNTk4LC
0xOTM3NzIxMzUxLC0zODUzMzU3MSwxOTc3MDgyOTA4LC02MjQ1
MDIxNjcsNDI1NDY4OTc5LC0yMDU0NTgzMTAxLDIxNDE0NDE5MD
YsMjA5MjYzNzcxNywtMTgzMzYyMTk2MywtOTgzMDE3OTc5LDk1
OTIxODA2Ml19
-->