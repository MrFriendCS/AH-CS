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

A clconstructor method, `__init__`, is used to create a new object.  It is called automatically when an object is created.

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
eyJoaXN0b3J5IjpbODg4MTU1MTk2LC0xNDQ4OTU2MTAyLDE4Mj
Y5OTcxNTYsLTQ3NTczMTgyMiw5OTczNzU2MTksLTE5MzI4NDg3
OSwtMTQxODU5OTY4LC0xMDg5MTM2MzczLDk1OTcyMjU5OCwtMT
kzNzcyMTM1MSwtMzg1MzM1NzEsMTk3NzA4MjkwOCwtNjI0NTAy
MTY3LDQyNTQ2ODk3OSwtMjA1NDU4MzEwMSwyMTQxNDQxOTA2LD
IwOTI2Mzc3MTcsLTE4MzM2MjE5NjMsLTk4MzAxNzk3OSw5NTky
MTgwNjJdfQ==
-->