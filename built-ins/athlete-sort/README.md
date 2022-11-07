# Athlete Sort

https://www.hackerrank.com/challenges/python-sort-sort

### Problem

You are given a spreadsheet that contains a list of N athletes and their details (such as age, height, weight and so on).   
You are required to sort the data based on the Kth attribute and print the final resulting table.

**Input Format**

The first line contains N and M separated by a space.   
The next N lines each contain M elements.   
The last line contains K.

**Output Format**

Print the N lines of the sorted table. Each line should contain the space separated elements. Check the sample below for clarity.

**Sample Input 0**

```
5 3
10 2 5
7 1 0
9 9 9
1 23 12
6 5 9
1
```

**Sample Output 0**

```
7 1 0
10 2 5
6 5 9
9 9 9
1 23 12
```

### My Solution

- [Python 2](python2.py)
- [Python 3](python3.py)
```python
n, m = map(int, input().split())

arr = [list(map(int, input().split())) for _ in range(n)]

k = int(input())

s = sorted(arr, key = lambda x: x[k])

[print(str.join(' ', map(str, s[i]))) for i in range(n)]
````