# What's Your Name?

https://www.hackerrank.com/challenges/whats-your-name

### Problem

You are given the firstname and lastname of a person on two different lines. Your task is to read them and print the following:

```
Hello firstname lastname! You just delved into python.
```

**Input Format**

The first line contains the first name, and the second line contains the last name.

**Output Format**

Print the output as mentioned above.

**Sample Input 0**

```
Ross
Taylor
````

**Sample Output 0**

```
Hello Ross Taylor! You just delved into python.
```

### My Solution

- [Python 2](python2.py)
- [Python 3](python3.py)
```python
def print_full_name(a, b):
    print("Hello %s %s! You just delved into python." % (a, b))

if __name__ == '__main__':
    first_name = input()
    last_name = input()
    print_full_name(first_name, last_name)
````