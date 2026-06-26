---
title: Day 7 of 100 Days of Python
date: 2026-06-26 21:26:00 +00:00
description: Practising Lists
categories: Coding
tags: Python
---
Today, I solved a List question in Python. The question was to accept values and save those in the list. Then, using a for loop, check if the number is greater than its immediate neighbours.

![image.png](assets/img/image-14.png)

```python
# A "Peak Element" is an element that is strictly greater than its neighbors (the element right before it and the element right after it).
# Write a program that scans a list of integers and prints all the peak elements along with their index positions.
# Constraints for simplicity: * Don't worry about the very first and very last elements of the list (since they don't have two neighbors). Just check everything in the middle.
# Example Walkthrough
# If your list is: [10, 20, 15, 25, 30, 22, 18]
# 20 is a peak because it's greater than 10 and 15.
# 30 is a peak because it's greater than 25 and 22.

a = []
print("Enter 10 numbers for list")
for i in range(0,10):
    value = int(input())
    a.append(value)
print("All values in a:")

for i in range(0,10):
    print(f"{a[i]}")

for i in range(1,9):
    if a[i]>a[i-1] and a[i]>a[i+1]:
        print(f"{a[i]} is greater than left value {a[i-1]} and right value {a[i+1]}")
```

