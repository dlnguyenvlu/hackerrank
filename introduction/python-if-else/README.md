# Python If-Else

https://www.hackerrank.com/challenges/py-if-else

**Task**

Given an integer, n, perform the following conditional actions:

If n is odd, print Weird
If n is even and in the inclusive range of 2 to 5, print Not Weird
If n is even and in the inclusive range of 6 to 20, print Weird
If n is even and greater than 20, print Not Weird

**Input Format**

A single line containing a positive integer, n.

**Output Format**

Print Weird if the number is weird; otherwise, print Not Weird.

### My Solution

- [Python 2](python2.py)
- [Python 3](python3.py)
```python
#!/bin/python3

N = int(input())

if N % 2 == 1:
    print("Weird")
elif N % 2 == 0 and N >= 6 and N <= 20:
    print("Weird")
else:
    print("Not Weird")
````