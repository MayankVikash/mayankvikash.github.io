---
title: Day 19 of 100 Days of Python
date: 2026-07-08 19:36:00 +00:00
description: Practising DSA
categories: Coding
tags: Python
---
First Program:

```python
underlying_array_size = 10;
user_keys = ["alpha", "beta", "gamma", "delta"];

for key in user_keys:
    s=0
    for i in key:
        s = s+ ord(i)
    ti = s%underlying_array_size
    print(f"Key '{key}' maps to array index: {ti}")
```

Output:

```
Key 'alpha' maps to array index: 8
Key 'beta' maps to array index: 2
Key 'gamma' maps to array index: 5
Key 'delta' maps to array index: 2
```

The second program today was to practise Bubble Sort for DSA.

```python
# Bubble Sort

def bubble_sort(arr):
    l = len(arr)
    for i in range(0,l):
        for j in range(0, l-i-1):
            if arr[j]>arr[j+1]:
                arr[j],arr[j+1] = arr[j+1], arr[j]
    return arr

arr = []

print("Enter the number of values ")
n = int(input())
print("Enter values of arrays ")

for i in range(0, n):
    i = int(input())
    arr.append(i)

print("Sorting is asccending order using Bubble Sort")
print(bubble_sort(arr))


```

Output:

```
Enter the number of values
5
Enter values of arrays
12
45
98
2
178
Sorting is asccending order using Bubble Sort
[2, 12, 45, 98, 178]
```

