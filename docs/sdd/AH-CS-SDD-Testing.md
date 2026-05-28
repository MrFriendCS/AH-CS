# Testing

Functions, records, and classes can be saved in seperate modules (`.py` files), and tested as standalone code.


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

Initially, the code in `try` is run.
If an exception is thrown, the code in `except` is then run.

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
