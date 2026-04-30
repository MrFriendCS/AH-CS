# Standard Algorithms


## Bubble Sort

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


## Insertion Sort

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


## Binary Search

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
