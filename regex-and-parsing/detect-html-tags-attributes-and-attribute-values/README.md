# Detect HTML Tags, Attributes and Attribute Values

https://www.hackerrank.com/challenges/detect-html-tags-attributes-and-attribute-values

**Problem**

You are given an HTML code snippet of N lines.  
Your task is to detect and print all the HTML tags, attributes and attribute values.  
  
Print the detected items in the following format:

```
Tag1
Tag2
-> Attribute2[0] > Attribute_value2[0]
-> Attribute2[1] > Attribute_value2[1]
-> Attribute2[2] > Attribute_value2[2]
Tag3
-> Attribute3[0] > Attribute_value3[0] 
```

**Input format**

The first line contains an integer N, the number of lines in the HTML code snippet.  
The next N lines contain HTML code.

**Output format**

Print the HTML tags, attributes and attribute values in order of their occurrence from top to bottom in the snippet.  
  
Format your answers as explained in the problem statement.

**Sample Input 0**

```
9
<head>
<title>HTML</title>
</head>
<object type="application/x-flash" 
  data="your-file.swf" 
  width="0" height="0">
  <!-- <param name="movie" value="your-file.swf" /> -->
  <param name="quality" value="high"/>
</object>
```

**Sample Output 0**

```
head
title
object
-> type > application/x-flash
-> data > your-file.swf
-> width > 0
-> height > 0
param
-> name > quality
-> value > high
```

### My Solution

- [Python 2](python2.py)
- [Python 3](python3.py)
```python
from html.parser import HTMLParser

class MyHTMLParser(HTMLParser):
    
    def print_attrs(self, attrs):
        [print("->", attr[0], ">", attr[1]) for attr in attrs]

    def handle_starttag(self, tag, attrs):
        print(tag)
        self.print_attrs(attrs)

    def handle_comment(self, data):
        pass
    
    def handle_startendtag(self, tag, attrs):
        print(tag)
        self.print_attrs(attrs)

html = str.join('', [input() for _ in range(int(input()))])

parser = MyHTMLParser()
parser.feed(html)
````