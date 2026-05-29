# Software

## Long lines of code

Long lines of code that have parentheses (round brackets) can be split over multiple lines.

``` python
print(1 + 2 +
      3 + 4)
      
print('Long lines of code '
      'can be broken up.')
```

Long lines of code without parentheses can use a backslash (`\`) to split them.

``` python
answer = 1 + 2 \
         + 3 + 4
      
print(answer)
```


## f Strings

``` python
pi = 3.14159265359

print(f'pi = {pi}')

print(f'pi = {pi:.4f} (4 dp)')

print(f'pi = {pi:.4g} (4 sf)')

print(f'Enjoy a raspberry pie for only £{pi*2:.2f}!')

```


## Combined Operators

Arithmetic operators can be combined with the assignment operator.

| Operator | Example | Meaning |
| :------: | :-----: | :-----: |
| +=       | x += 3  | x = x + 3 |
| -=       | x -= 3  | x = x - 3 |
| *=       | x *= 3  | x = x * 3 |
| /=       | x /= 3  | x = x / 3 |
| %=       | x %= 3  | x = x % 3 |
| //=      | x //= 3 | x = x // 3 |
| **=      | x **= 3 | x = x ** 3 |


## Import


### All Code

To import all functions, records, and classes from a module use `import` _module name_.

``` python
import random

print(random.randint(1, 6))
```


### Specific Code

To import individual functions, records, and classes from a module use `from` _module name_ and `import` _object name_.

``` python
from random import randint

print(randint(1, 6))
```