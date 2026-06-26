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
#  Ignore the very first and very last elements of the list (since they don't have two neighbors).
# Example
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

This is the second Program of the day:

![image.png](assets/img/image-15.png)

```python
# Write a program from scratch that does the following:
# Create a list containing 8 numbers of your choice (you can hardcode this list directly into the program, no need to take inputs for the array creation unless you want to).
# Take a single integer input from the user— this will be the target_value they want to search for.
# Use a loop to scan the list. If the target_value exists in the list, print the index position where it was found.
#  If the number appears multiple times in your list, print every index position where it shows up.
# If the loop completes and the number wasn't found anywhere in the list, print "Value not found in the sequence."
a = [1,2,3,4,5,6,7,8]
found = False
s = int(input("Enter the number to be searched"))
for i in range(0,8):
    if a[i]==s:
        found = True
        print(f"found at position: {i}")
if found:
    print("Number found at above values")
else:
    print("Value not found in the sequence")
```

