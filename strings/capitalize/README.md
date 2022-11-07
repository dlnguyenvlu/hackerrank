# Capitalize!

https://www.hackerrank.com/challenges/capitalize

### Problem

You are asked to ensure that the first and last names of people begin with a capital letter in their passports. For example, alison heck should be capitalised correctly as Alison Heck.

alison heck => Alison Heck

Given a full name, your task is to capitalize the name appropriately.

**Input Format**

A single line of input containing the full name, S.

**Output Format**

Print the capitalized string, S.

**Sample Input 0**

```
chris alan
```

**Sample Output 0**

```
Chris Alan
```

### My Solution

- [Python 2](python2.py)
- [Python 3](python3.py)
```python
#!/bin/python3

import math
import os
import random
import re
import sys

# Complete the solve function below.
def solve(s):
    return ' '.join([word.capitalize() for word in s.split(' ')])

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    s = input()

    result = solve(s)

    fptr.write(result + '\n')

    fptr.close()

````