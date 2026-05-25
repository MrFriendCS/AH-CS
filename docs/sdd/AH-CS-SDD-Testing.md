# Testing

Functions, records, and classes can be saved in seperate modules (`.py` files), and tested as standalone code.


## Import


### All Code

To import all functions, records, and classes from a module use `import`.

``` python
import random

print(random.randint(1, 6))
```


### Specific Code

To import individual functions, records, and classes from a module use `from` and `import`.

``` python
from random import randint

print(randint(1, 6))
```


## Assert

``` python
# Will pass
assert 1 == 1

# Will throw an exception
assert 1 == 2
```


## Try, Except

``` python
try:
    # Will pass
    assert 1 == 1
    print('Pass: 1==1')
except:
    print('Fail: 1==1')

try:
    # Will throw and exception
    assert 1 == 2
    print('Pass: 1==2')
except:
    print('Fail: 1==2')
```
