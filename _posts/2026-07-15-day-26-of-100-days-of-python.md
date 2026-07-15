---
title: Day 26 of 100 Days of Python
date: 2026-07-15 01:16:00 +00:00
description: Practising DSA
categories: Coding
tags: Python
---
Today I started with Sets Data Structures.

```python
r_scans = ["Alice", "Bob", "Alice", "Charlie", "Bob", "David"]
unique_attendance = set(r_scans)
print("Eve" in unique_attendance)
print(unique_attendance)

```

Output:

```
False
{'David', 'Bob', 'Charlie', 'Alice'}
```

The second program I did was Linear Search.

```python
inventory = [104, 201, 355, 402, 589, 612]

def linear_search(arr, target):
    for i in range(0,len(arr)):
        if arr[i] == target:
            return i
    return -1

r = linear_search(inventory, 402)
print(r)
```

