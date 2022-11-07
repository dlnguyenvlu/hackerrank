# sWAP cASE

https://www.hackerrank.com/challenges/swap-case

### Problem

You are given a string and your task is to swap cases. In other words, convert all lowercase letters to uppercase letters and vice versa.

**For Example** 

```
Www.HackerRank.com → wWW.hACKERrANK.COM
Pythonist 2 → pYTHONIST 2
```

**Input Format**

A single line containing a string S.

**Output Format**

Print the modified string S.

**Sample Input 0**

```
HackerRank.com presents "Pythonist 2".
````

**Sample Output 0**

```
hACKERrANK.COM PRESENTS "pYTHONIST 2".
```

### My Solution

- [Python 2](python2.py)
- [Python 3](python3.py)
```python
def swap_case(s):

    return ''.join([c.lower() if c.isupper() else c.upper() for c in s])

if __name__ == '__main__':
    s = input()
    result = swap_case(s)
    print (result)
````