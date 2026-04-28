# Software Design and Development


## Notes

All the code examples use Python.

These notes are focused on Advanced Higher Computing Science so some terms may be used differently.


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
