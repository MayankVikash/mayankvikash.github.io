---
title: Day 4 of 100 Days of Python
date: 2026-06-23 10:27:00 +00:00
description: Practising Nested Loop
categories: Coding
tags: Python
---
Today, I started Nested Loop. It is a for or while loop running inside another loop. It is mainly used for executing repetitive tasks, while another macro task is simultaneously being executed.  


![Screenshot of code](assets/img/image-9.png)



```python
# Write a program that inputs the number of rows and columns, then prints an alternating matrix of 1s and 0s where the element is 1 if the sum of its row and column indices is even, and 0 otherwise

r = int(input("Enter number of rows "))
c = int(input("Enter number of columns "))


for i in range(0,r):
        for j in range(0,c):
            s = i + j
            if s%2==0:
                print(1, end=" ")
            else:
                print(0, end=" ")
        print()
```

The question for this program was to input the number of rows and columns into two different variables. And create a matrix, but at the position where the row value and column value add up to an even, a 1 should be placed there. And where they add up to an odd number, a 0 should be placed.

