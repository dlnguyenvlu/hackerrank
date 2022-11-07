# List Comprehensions

https://www.hackerrank.com/challenges/list-comprehensions

### Problem

Let's learn about list comprehensions! You are given three integers X, Y and Z representing the dimensions of a cuboid along with an integer N. 
You have to print a list of all possible coordinates given by (i, j, k) on a 3D grid where the sum of i + j + k is not equal to N. 
Here, 0 < i < X, 0 < j < Y, 0 < k < Z.


**Input Format**

Four integers X, Y, Z and N each on four separate lines, respectively.

**Output Format**

For each command of type print, print the list on a new line.

**Sample Input 0**
```
1
1
1
2
```

**Sample Output 0**
```
[[0, 0, 0], [0, 0, 1], [0, 1, 0], [1, 0, 0], [1, 1, 1]]
```

### My Solution

- [Python 2](python2.py)
- [Python 3](python3.py)
```python
if __name__ == '__main__':

    x = int(input())
    y = int(input())
    z = int(input())
    n = int(input())

    coords = [[nx, ny, nz] for nx in range(x + 1) 
                           for ny in range(y + 1) 
                           for nz in range(z + 1) 
                           if nx + ny + nz != n]

    print(coords)
````