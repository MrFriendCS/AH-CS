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

The keyword `assert` is used for testing.
If the assertion is incorrect, an exception is thrown.

``` python
# Will not throw an exception
assert 1 == 1

# Will throw an exception
assert 1 == 2
```


### Try, Except

The code in keyword `try` is run.
If an exeption is thrown, the code in keyword `except` is then run.

``` python
# Will not throw an exception
try:
    assert 1 == 1
    print('Pass: 1 == 1')

except:
    print('Fail: 1 == 1')


# Will throw an exception
try:
    assert 1 == 2
    print('Pass: 1 == 2')

except:
    print('Fail: 1 == 2')
```
