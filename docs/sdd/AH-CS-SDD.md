# Software

## Long lines of code

Use a backslash (`\`) to break up long lines of code.

``` python
print('Long lines of code ' \
      + 'can be broken up.')
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
