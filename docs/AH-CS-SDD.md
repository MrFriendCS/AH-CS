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

It is normal for the `self` to be the first parameter of any method.  `self` refers to the current object.

Properties are kept private by using a double underscore (`__`) before the name of the property.  Getter and setter methods will need to be provided to access or update the value of the property.

``` python
class Person:
    """Declare a class to define a person."""

    def __init__(self, name="", age=0):
        """Object constructor method.  Automatically called when an object is created."""
        # Class properties
        self.__name = name  # Private property
        self.__age = age    # Private property

    def getAge(self):
        """Getter method for age."""
        return self.__age

    def setAge(self, age=0):
        """Setter method for age."""
        self.__age = age
```

An example of instantiation, creating and object, is shown below:

``` python
# Create a new object
newPerson = Person("Tom", 18)

# Display their age
print(newPerson.getAge())
```

### Inheritance

New classes can be declared that inherit the characteristics of a class, and extend with additional properties and / or methods.

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
eyJoaXN0b3J5IjpbLTE4ODA3NDY1MzksNDIwMjQ2MDM0LDE5Mj
c0ODExMTIsLTE4NzczMjc5MDQsLTE0NDg5NTYxMDIsMTgyNjk5
NzE1NiwtNDc1NzMxODIyLDk5NzM3NTYxOSwtMTkzMjg0ODc5LC
0xNDE4NTk5NjgsLTEwODkxMzYzNzMsOTU5NzIyNTk4LC0xOTM3
NzIxMzUxLC0zODUzMzU3MSwxOTc3MDgyOTA4LC02MjQ1MDIxNj
csNDI1NDY4OTc5LC0yMDU0NTgzMTAxLDIxNDE0NDE5MDYsMjA5
MjYzNzcxN119
-->