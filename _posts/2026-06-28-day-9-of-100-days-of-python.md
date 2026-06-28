---
title: Day 9 of 100 Days of Python
date: 2026-06-28 21:05:00 +00:00
description: Practising Functions
categories: Coding
tags: Python
---
Today is Day 9 of the challenge. I learned about Functions in Python today and created this simple program.

![image.png](assets/img/image-18.png)

```python
def sarea(s):
    area = s*s
    return area
def rperi(l,b):
    p = 2*(l+b)
    return p
def check(n):
    if n%2==0:
        return "Even"
    else:
        return "Odd"
ch = int(input("Enter 1 to find square area, 2 for rectangle permimeter and 3 to check if the input number is even or odd"))
if ch ==1:
    side = int(input("Enter the side of square"))
    print(f"Area is: {sarea(side)}")
elif ch ==2:
    l = int(input("Enter the length of rectangle"))
    b = int(input("Enter the breath of rectangle"))
    print(f"Perimeter is: {rperi(l,b)}")
elif ch ==3:
    num = int(input("Enter the number to check"))
    print(f"Number is: {check(num)}")
else:
    print("Invalid input")
```

