# Software Design and Development


## Notes

All the code examples use Python.

These notes are focused on Advanced Higher Computing Science so some terms may be used differently.


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
