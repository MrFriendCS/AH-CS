# Object-Orientated Programming (OOP)

Classes create objects.  Objects have properties and methods.

An object is a way of representing _something_ in software, e.g. a person or a vehicle.
Objects have instance variables, also known as properties, and methods:

* Instance variable - something about the object (property: data)
* Method - something the object can do (a sub-program: behaviour)


## Declaration

The `class` keyword is used to declare the _blueprint_ for new objects.
New classes are named using `CapitalisedWords`.

A class contains a constructor method, `__init__`, which is used to create a new object.
It is called automatically when an object is created.

It is normal for `self` to be the first parameter of any method.  `self` refers to the current object.

Properties and methods are kept private by using a double underscore (`__`) before the name of a property or method.
If a property or method is private, it can only be accessed from within the object.
This is know as ___encapsulation___.
Accessor (getter) and mutator (setter) methods will need to be provided to access or change the value of a private property.

``` python
class Person:
    """A class to define a person."""

    def __init__(self, name: str='TBC', age: int=0):
        """Object constructor method. """ \
        + """Automatically called when an object is created."""
        
        # Class properties - Private
        self.__name = name
        self.__age = age

    def get_age(self) -> int:
        """Getter method for age."""
        return self.__age

    def set_age(self, age: int=0) -> None:
        """Setter method for age."""
        self.__age = age
    
    def get_name(self) -> str:
        """Getter method for name."""
        return self.__name
        
    def info(self) -> tuple:
        """Method to access person information."""
        
        return self.__name, self.__age
```

An example of instantiation, creating an object, is shown below:

``` python
# Create a new object
new_person = Person('Tom', 25)

# Display their age
print(new_person.get_age())
```


## Inheritance and Overriding

New classes can be declared that inherit the properties and methods of an existing class. 
The new class can be extend with additional properties and / or methods.

A method can be overridden with a new method of the same name.

``` python
class Pupil(Person):
    """A class to define a pupil.  Inherits from the Person class."""

    def __init__(self, name: str='TBC', age: int=5, year_group: str='P1'):
        """Object constructor method. """ \
        """Automatically called when an object is created."""
        
        # Use superclass initilisation
        super().__init__(name, age)
        
        # Sub-class property - Private
        self.__year_group = year_group

    def get_year_group(self) -> str:
        """Getter method for year_group."""
        return self.__year_group

    def set_year_group(self, year_group: str='P1') -> None:
        """Setter method for year_group."""
        self.__year_group = year_group
        
    def info(self) -> tuple:
        """Method to access pupil information.""" \
        + """Overwrites superclass method."""
        
        return self.get_name(), self.get_age(), self.__year_group
```

An example is shown below:

``` python
# Create a new object
new_pupil = Pupil('Emma', 17, 'S5')

# Display their age - Encapulation!
print(new_pupil.get_age())
```

Example of overiding is shown below:

``` python
# Introduce the person
details = new_person.info()
print(f'Hi, I\'m {details[0]}.  I\'m {details[1]} years old.')

# Introduce the pupil
details = new_pupil.info()
print(f'Hi, I\'m {details[0]}.  I\'m {details[1]} years old and in {details[2]}.')
```


## Array of objects

The data to create an array of objects could be read from a file.

``` python
# Data for the objects
people = ['Alan,24','Beth,23','Carl,22','Dina,21']
```

Create an empty array.

```
# Empty array
array_of_objects = []
```

Loop for each object, create an object and append to the empty array

``` python
# Populate array
for index in range(len(people)):
    
    # Split data at comma
    data = people[index].split(',')
    
    # Extract values
    name = data[0]
    age = int(data[1])
    
    # Create new object and append to array
    array_of_objects.append(Person(name, age))
```

Loop for each object in array.

```
# Loop for each object
for index in range(len(array_of_objects)):
    
    # Get info about the current object
    details = array_of_objects[index].info()
    
    # Display info about the current object
    print(f'Hi, I\'m {details[0]}.  I\'m {details[1]} years old.')
```
