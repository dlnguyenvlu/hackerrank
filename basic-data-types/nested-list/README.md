# Lists

https://www.hackerrank.com/challenges/nested-list

### Problem

Given the names and grades for each student in a Physics class of N students, store them in a nested list and print the name(s) of any student(s) having the second lowest grade.

Note: If there are multiple students with the same grade, order their names alphabetically and print each name on a new line.

**Input Format**

The first line contains an integer, N, the number of students. 

The 2N subsequent lines describe each student over 2 lines; the first line contains a student's name, and the second line contains their grade.

**Output Format**

Print the name(s) of any student(s) having the second lowest grade in Physics; if there are multiple students, order their names alphabetically and print each one on a new line.

**Sample Input 0**
```
5
Harry
37.21
Berry
37.21
Tina
37.2
Akriti
41
Harsh
39
```

**Sample Output 0**
```
Berry
Harry
```

### My Solution

- [Python 2](python2.py)
- [Python 3](python3.py)
```python
students = list()

for _ in range(int(input())):

    name = input()

    score = float(input())

    students.append([name, score])

# order by score
students.sort(key = lambda x: x[1])

# get the first lowest score
first = students[0][1]

# find the second lowest score
for student in students:
    if student[1] > first:
        second = student[1]
        break

# order by name
students.sort(key = lambda x: x[0])

for student in students:
    if student[1] == second:
        print(student[0])
````