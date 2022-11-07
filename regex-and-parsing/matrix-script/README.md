# Matrix Script

https://www.hackerrank.com/challenges/matrix-script

### Problem
 
Neo has a complex matrix script. The matrix script is a N X M grid of strings. It consists of alphanumeric characters, spaces and symbols (!,@,#,$,%,&).

To decode the script, Neo needs to read each column and select only the alphanumeric characters and connect them. Neo reads the column from top to bottom and starts reading from the leftmost column.

If there are symbols or spaces between two alphanumeric characters of the decoded script, then Neo replaces them with a single space '' for better readability.

Neo feels that there is no need to use 'if' conditions for decoding.

Alphanumeric characters consist of: [A-Z, a-z, and 0-9].

**Input format**

The first line contains space-separated integers N (rows) and M (columns) respectively. 
The next N lines contain the row elements of the matrix script.

**Output format**

Print the decoded matrix script.

**Sample Input 0**

```
7 3
Tsi
h%x
i #
sM 
$a 
#t%
ir!
```

**Sample Output 0**

```
This is Matrix#  %!
```

### My Solution

- [Python 2](python2.py)
- [Python 3](python3.py)
```python
import re

n, m = map(int, input().split())

matrix = [input() for _ in range(n)]

traversed = [matrix[j][i] for i in range(m) for j in range(n)]

pattern = r'([a-z0-9])([^a-z0-9]+)([a-z0-9])'

decoded = re.sub(pattern, r'\1 \3', str.join('', traversed), 0, re.I) 

print(decoded)
````