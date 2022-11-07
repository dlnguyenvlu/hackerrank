# Find a string

https://www.hackerrank.com/challenges/find-a-string

### Problem

In this challenge, the user enters a string and a substring. 
You have to print the number of times that the substring occurs in the given string. 
String traversal will take place from left to right, not from right to left.


**Input Format**

The first line of input contains the original string. The next line contains the substring.

**Output Format**

Output the integer number indicating the total number of occurrences of the substring in the original string.

**Sample Input 0**

```
ABCDCDC
CDC
```

**Sample Input 0**

```
2
```

### My Solution

- [Python 2](python2.py)
- [Python 3](python3.py)
```python
def count_substring(string, sub_string):
    return sum([1 for i in range(0, len(string) - len(sub_string) + 1) if string[i:i+len(sub_string)] == sub_string])
            

if __name__ == '__main__':
    string = input().strip()
    sub_string = input().strip()
    
    count = count_substring(string, sub_string)
    print(count)
````