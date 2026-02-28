# Software Design and Development

## Notes

All the code examples use Python.

These notes are focused on Advanced Higher Computing Science so some terms may be used differently.

## Objects

An object is a way of representing _something_ in software, e.g. a person or a vehicle.  A string, such as "Hello", is an object.  An object will have properties and methods:

* Property - something about the object (a variable: data)
* Method - something the object can do (a sub-program: behaviour)

### Declaration

The `class` keyword is used to declare the _blueprint_ for new objects.  New classes are named using `CapitalisedWords`.

``` python
class Person:
    """Declare a class to define a person."""

    # Class properties
    name = "Tom"
    age = 18
```

An example of using this class is:

``` python
# Create a new object
newPerson = Person()

# Access a property
print(newPerson.name)
```

``` python
class Person:
    """Declare a class to define a person."""


    def __init__(self, name="", age=0):
        """Object constructor method.  Automatically called when an object is created."""
        
        # Class properties
        self.name = name  # Private property
        self.age = age    # Private property
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
eyJoaXN0b3J5IjpbODIwNzcyNDEzLDk5NzM3NTYxOSwtMTkzMj
g0ODc5LC0xNDE4NTk5NjgsLTEwODkxMzYzNzMsOTU5NzIyNTk4
LC0xOTM3NzIxMzUxLC0zODUzMzU3MSwxOTc3MDgyOTA4LC02Mj
Q1MDIxNjcsNDI1NDY4OTc5LC0yMDU0NTgzMTAxLDIxNDE0NDE5
MDYsMjA5MjYzNzcxNywtMTgzMzYyMTk2MywtOTgzMDE3OTc5LD
k1OTIxODA2MiwxNjEyMjcwMzMyLDczOTQ4MzI2Myw2OTU0MjU1
OTldfQ==
-->