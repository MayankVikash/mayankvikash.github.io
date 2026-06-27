---
title: Day 8 of 100 Days of Python
date: 2026-06-27 22:24:00 +00:00
description: Practising Bubble Sort
categories: Coding
tags: Python
---
Today is Day 8 of the 100 Days of Python. Today, I created a Bubble Sort problem.

![image.png](assets/img/image-16.png)

```python
# Bubble Sort
a = []
n = int(input("Enter the no. of values in the list"))
print("Enter values of the list ")
for i in range(0,n):
    v = int(input())
    a.append(v)
print("This is current list:")
print(a)
for i in range(0, n):
    for j in range(0,n-1):
        if a[j]>a[j+1]:
            a[j], a[j+1] = a[j+1], a[j]
    print(f"List after iteration {i}:")
    print(a)

print("List sorted in ascending order:")
print(a)
```

