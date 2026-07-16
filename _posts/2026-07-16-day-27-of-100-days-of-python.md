---
title: Day 27 of 100 Days of Python
date: 2026-07-16 21:33:00 +00:00
description: Practising DSA
categories: Coding
tags: Python
---
Today, I practised Merge Sort algorithm. It divides the list/array in two parts from mid using recursion, until only 1 element is left in each list. After that, it merges them both in another empty list and sorting them while doing so.

```python
# Merge Sort

data = [38, 27, 43, 3, 9, 82, 10]

def merge_sort(arr):
    if len(arr) == 1 or len(arr) ==0:
        return arr
    mid = len(arr)//2
    left_half = merge_sort(arr[:mid])
    right_half = merge_sort(arr[mid:])
    sorted_arr=[]
    i=j=0
    while i<len(left_half) and j<len(right_half):
        if left_half[i]<right_half[j]:
            sorted_arr.append(left_half[i])
            i+=1
        else:
            sorted_arr.append(right_half[j])
            j+=1
    sorted_arr.extend(left_half[i:])
    sorted_arr.extend(right_half[j:])
    return sorted_arr
print(merge_sort(data))

```

Output:

```
[3, 9, 10, 27, 38, 43, 82]
```

