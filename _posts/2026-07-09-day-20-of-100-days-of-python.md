---
title: Day 20 of 100 Days of Python
date: 2026-07-09 20:31:00 +00:00
description: Practising DSA
categories: Coding
tags: Python
---
The first question I did today was Insertion Sort. In this sorting algorithm, the first element of a list/array is assumed to be sorted, while the next element is compared to the previous one, and if the previous element is larger than it is stored in a variable key and shifted to the right.

```python
# Insertion Sort
def insertion_sort(arr):
    for i in range(1,len(arr)):
        key = arr[i]
        j = i-1
        while j>=0 and arr[j]>key:
            arr[j+1] = arr[j]
            j-=1
        arr[j+1] = key
    return arr
cards = [12, 11, 13, 5, 6]
print(insertion_sort(cards))
```

Output for Program 1:

```
[5, 6, 11, 12, 13]
```

