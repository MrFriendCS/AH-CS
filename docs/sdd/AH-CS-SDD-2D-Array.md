# 2D Array

A 2D array is an array of arrays.

``` python
# Define size of 2D array
rows: int = 3
cols: int = 5

# Create 2D array
two_d_array: list[list[int]] = [[0 for _ in range(cols)] for _ in range(rows)]

# Change a single element
two_d_array [0][0] = 1
two_d_array [1][2] = 2
two_d_array [2][4] = 3

# Display 2D array
print(two_d_array, "\n")

# Dsiplay 2D array, row by row
for row in two_d_array:

    print(row)
```
