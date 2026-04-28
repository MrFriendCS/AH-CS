# Software Design and Development


## Notes

All the code examples use Python.

These notes are focused on Advanced Higher Computing Science so some terms may be used differently.


## Object-Orientated Programming (OOP)

Classes create objects.  Objects have properties and methods.

An object is a way of representing _something_ in software, e.g. a person or a vehicle.
Objects have properties and methods:

* Property - something about the object (a variable: data)
* Method - something the object can do (a sub-program: behaviour)


### Declaration

The `class` keyword is used to declare the _blueprint_ for new objects.
New classes are named using `CapitalisedWords`.

A class contains a constructor method, `__init__`, which is used to create a new object.
It is called automatically when an object is created.

It is normal for `self` to be the first parameter of any method.  `self` refers to the current object.

Properties and methods are kept private by using a double underscore (`__`) before the name of a property or method.
If a property or method is private, it can only be accessed from within the object.
Getter and setter methods will need to be provided to access or update the value of a private property.

``` python
class Person:
    """Declare a class to define a person."""

    def __init__(self, name="", age=0):
        """Object constructor method.  Automatically called when an object is created."""
        
        # Class properties - Private
        self.__name = name
        self.__age = age

    def getAge(self):
        """Getter method for age."""
        return self.__age

    def setAge(self, age=0):
        """Setter method for age."""
        self.__age = age
```

An example of instantiation, creating an object, is shown below:

``` python
# Create a new object
newPerson = Person("Tom", 18)

# Display their age
print(newPerson.getAge())
```


### Inheritance

New classes can be declared that inherit the properties and methods of an existing class. 
The new class can be extend with additional properties and / or methods.

``` python
class Pupil(Person):
    """Declare a class to define a pupil.  Inherits from the Person class."""

    def __init__(self, name="", age=0, yearGroup="P1"):
        """Object constructor method.  Automatically called when an object is created."""
        
        # Use super class initilisation
        super().__init__(name, age)
        
        # Class property - Private
        self.__yearGroup = yearGroup

    def getYearGroup(self):
        """Getter method for yearGroup."""
        return self.__yearGroup

    def setYearGroup(self, yearGroup="P1"):
        """Setter method for yearGroup."""
        self.__yearGroup = yearGroup
```

An example is shown below:

``` python
# Create a new object
newPupil= Pupil("Emma", 17, "S5")

# Display their age
print(newPupil.getAge())
```


## Standard Algorithms


### Bubble Sort

``` python
array = [7, 2, 6, 5, 4, 3, 1]

# Get number of elements
n = len(array)

# Turn sort on
sort = True

# Sort if needed
while sort == True:
    
    # Turn sort off
    sort = False
    
    # Loop from start of array
    for index in range(n - 1):
        
        # Compare current element with next element
        if array[index] > array[index + 1]:
            
            # Swap values
            temp = array[index]
            array[index]  = array[index + 1]
            array[index + 1] = temp
            
            # Sorting still needed
            sort = True
    
    # Reduce the number elements to be checked
    n = n - 1
```


### Insertion Sort

``` Python
array = [7, 2, 4, 5, 3, 6, 1]

currentValue = 0
position = 0

# Loop over array
for index in range(1, len(array)):
    
    # Get current value from array
    currentValue = array[index]
    
    # Get current position
    position = index
    
    # Loop if current value is larger then value to the left
    while (position > 0) and (currentValue < array[position-1]):
        
        # Move value left
        array[position] = array[position-1]
        
        # Decrement position
        position = position - 1
    
    # Set current position to the original value
    array[position] = currentValue
```


### Binary Search

``` Python
array = [1, 2, 3, 4, 5, 6, 7]
target = 5

# First and last index of array
start = 0
end = len(array) - 1

# Result
found = False

# Loop until found, or all elements checked
while not found and (start <= end):
    
    # Calculate mid point of array to be searched
    mid = int((start + end) / 2)
    
    # Check if found
    if array[mid] == target:
        
        # Update result
        found = True
    
    # Check if target value is greater than current value
    elif array[mid] > target:
        
        # Update end of array to be searched
        end = mid - 1
        
    else:
        
        # Update start of array to be searched
        start = mid + 1
```

## 2D Array

A 2D array is an array of arrays.

``` python
# Define size of 2D array
rows = 3
cols = 5

# Create 2D array
array2d = [[0 for width in range(cols)] for height in range(rows)]

# Change a single element
array2d [1][2] = 5

# Display 2D array
print(array2d)

# Dsiplay 2D array, row by row
for row in array2d:
    
    print(row)
```


## Linked List

### Single Linked List

``` python
class NodeSingle:
    """Declare a class to define a singly linked list node."""

    def __init__(self, data=None, nextPointer=None):
        """Object constructor method.  Automatically called when an object is created."""

        # Class properties - Private
        self.__data = data
        self.__nextPointer = nextPointer
    
    def __str__(self):
        """Overwrite print()."""
        return f"Data: {self.__data}"
    
    
    # Class methods - Public

    def getData(self):
        """Getter method for data."""
        return self.__data

    def setData(self, data=None):
        """Setter method for data."""
        self.__data = data
    
    def getNext(self):
        """Getter method for pointer to next node."""
        return self.__nextPointer

    def setNext(self, nextPointer=None):
        """Setter method for pointer to next node."""
        self.__nextPointer = nextPointer
```

``` python
def traverseLinkedList(head):
    """Traverse a singly linked list from head to tail."""
    
    # Loop while linked to next node
    while head.getNext() != None:
        
        # Display current node data
        print(head.getData())
        
        # Move to next node
        head = head.getNext()
    
    # Display tail (last) node data
    print(head.getData())
```


``` python
# Create nodes
node1 = Node(12)
node2 = Node(3)
node3 = Node(19)

# Link nodes
node1.setNext(node2)
node2.setNext(node3)

# Traverse nodes
traverseLinkedList(node1)
```
