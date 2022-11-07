# Triangle Quest

https://www.hackerrank.com/challenges/python-quest-1

**Problem**

You are given a positive integer N. Print a numerical triangle of height N - 1 like the one below:

```
1
22
333
4444
55555
......
```

**Task**

Can you do it using only arithmetic operations, a single for loop and print statement?  
  
Use no more than two lines. The first line (the for statement) is already written for you. You have to complete the print statement.   

Note: Using anything related to strings will give a score of 0.  

**Input Format**  
A single line containing integer, N.

**Output Format**  
Print N - 1 lines as explained above.

**Sample Input 0**

```
5
```

**Sample Output 0**

```
1
22
333
4444
```

### My Solution

- [Python 2](python2.py)
- [Python 3](python3.py)
```python
for i in range(1,int(input())):
    print(int(i*(10**(i-1))+i*(10**(i-2))+i*(10**(i-3))+i*(10**(i-4))+i*(10**(i-5))+i*(10**(i-6))+i*(10**(i-7))+i*(10**(i-8))+i*(10**(i-9))))
````