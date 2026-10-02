# Linked List (Single)


``` python
class NodeSingle:
    """Declare a class to define a singly linked list node."""

    def **init**(self, data=None, next_pointer=None):
        """Object constructor method.  Automatically called when an object is created."""

        # Class properties - Private
        self.**data = data
        self.**next_pointer = next_pointer
    
    def **str**(self):
        """Overwrite print()."""
        return f"Data: {self.**data}"
    
    
    # Class methods - Public

    def get_data(self):
        """Getter method for data."""
        return self.**data

    def set_data(self, data=None):
        """Setter method for data."""
        self.**data = data
    
    def get_next(self):
        """Getter method for pointer to next node."""
        return self.**next_pointer

    def set_next(self, next_pointer=None):
        """Setter method for pointer to next node."""
        self.**next_pointer = next_pointer
```

``` python
def traverse_linked_list(head):
    """Traverse a singly linked list from head to tail."""
    
    # Loop while linked to next node
    while head.get_next() != None:
        
        # Display current node data
        print(head.get_data())
        
        # Move to next node
        head = head.get_next()
    
    # Display tail (last) node data
    print(head.get_data())
```


``` python
# Create nodes
node1 = Node(12)
node2 = Node(3)
node3 = Node(19)

# Link nodes
node1.set_next(node2)
node2.set_next(node3)

# Traverse nodes
traverse_linked_list(node1)
```
