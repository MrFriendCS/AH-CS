# Software Design and Development

## Notes

All the code examples use Python.

These notes are focused on Advanced Higher Computing Science so some terms may be used differently.

## Object Orientate

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

An example of using this class is:

``` python
# Create a new object
newPerson = Person(("Tom", 18)

# Access a property
print(newPerson.name)
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
eyJoaXN0b3J5IjpbNDcyMDI1OTM4LDE4MjY5OTcxNTYsLTQ3NT
czMTgyMiw5OTczNzU2MTksLTE5MzI4NDg3OSwtMTQxODU5OTY4
LC0xMDg5MTM2MzczLDk1OTcyMjU5OCwtMTkzNzcyMTM1MSwtMz
g1MzM1NzEsMTk3NzA4MjkwOCwtNjI0NTAyMTY3LDQyNTQ2ODk3
OSwtMjA1NDU4MzEwMSwyMTQxNDQxOTA2LDIwOTI2Mzc3MTcsLT
E4MzM2MjE5NjMsLTk4MzAxNzk3OSw5NTkyMTgwNjIsMTYxMjI3
MDMzMl19
-->