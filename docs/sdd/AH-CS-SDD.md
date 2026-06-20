# Software


## Style Conventions


### Naming

* Class: ThisIsAClass
* Property: this_is_a_property
* Method: this_is_a_method
* Function: this_is_a_function


### Blank lines

* Class: two lines before and after
* Function: two lines before and after
* Method: one line before and after


### Line Length

* Maximum: 72 characters


## Long lines of code

Long lines of code that have parentheses (round brackets) can be split over multiple lines.

``` python
print(1 + 2
      + 3 + 4)
      
print('Long lines of code '
      'can be broken up.')
```

Long lines of code without parentheses can use a backslash (`\`) to split them.

``` python
answer = 1 + 2 \
         + 3 + 4
      
print(answer)
```

__Note__: an operator should be at the start of the new line.


## String Formatting

An f-string can be used instead of concatenating variables.

``` python
pi = 3.14159265359

print(f'pi = {pi}')
```

An f-string can be formatted.

``` python
print(f'pi = {pi:.4f} (4 dp)')

print(f'pi = {pi:.4g} (4 sf)')
```

An f-string can include a calculation.

``` python
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


## Dummy Variables

When a loop variable is not going to be used in a loop, then an underscore (`_`) can be used instead of a variable name.
Using an underscore can make it clearer that the loop variable is not used in the loop.

``` python
for _ in range(5):

    print('Hi')
```


## main()

Functions in a program can be tested if all code is within functions.
However, if the file is imported by another file to be tested, it should not run.
This can be achieved by adding the following code.

``` python
if __name__ == '__main__': main()
```


## Import


### All Code

To import all functions, records, and classes from a module use `import` _module name_.

``` python
import random

print(random.randint(1, 6))
```


### Specific Code

To import individual functions, records, or classes from a module use `from` _module name_ and `import` _object name_.

``` python
from random import randint

print(randint(1, 6))
```

To import multiple functions, records, or classes, they can be named individualy.

``` python
from random import randint, sample

print(randint(1, 6))
print(sample([1, 2, 4, 9, 16, 25, 36, 49, 64, 81, 100], 3))
```