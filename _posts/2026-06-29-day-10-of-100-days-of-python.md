---
title: Day 10 of 100 Days of Python
date: 2026-06-29 20:21:00 +00:00
description: Practising Functions and Matrix
categories: Coding
tags: Python
---
Today on Day 10, I practised more programming questions based on Python Functions.

![image.png](assets/img/image-19.png)

```python
# Write a function called swap(arr) that finds the largest and smallest numbers in a list and swaps their positions.
# data = [30, 10, 40, 50, 20]
# Create a function swap(arr).
# Inside that function, use loops to locate the index of the minimum value and the index of the maximum value.
# Use Python swap (a, b = b, a) to swap those two elements at their respective index positions.
# Print the list before calling the function and after calling the function in your main program to verify the extremes successfully traded places.

def swap(list,l):
    max =0
    min =0
    for i in range(0, l):
        if list[max]<list[i]:
            max = i
        if list[min]>list[i]:
            min = i
    list[max], list[min] = list[min],list[max]


a = []
n = int(input("Enter the number of values in list "))
print("Enter values ")
for i in range(0,n):
    a.append(int(input()))
l = len(a)
print(f"The original list:\n{a}")
swap(a,l)
print(f"Swapped List: \n{a}")
```

The second program today was to calculate the sum of the diagonals of a matrix.

```python
# A 3x3 Grid (Matrix)
# matrix = [
#     [1, 2, 3],  # Row 0
#     [4, 5, 6],  # Row 1
#     [7, 8, 9]   # Row 2
# ]

m = [
    [1,2,4],
    [6,2,7],
    [5,3,9]
]
s=0
for r in m:
    print(r)
for i in range(0,3):
    s = s+m[i][i]
    print(f"Diagonals: {m[i][i]}")
print(f"Sum of diagonlas: {s}")
```

Output

```
[1, 2, 4]
[6, 2, 7]
[5, 3, 9]
Diagonals: 1
Diagonals: 2
Diagonals: 9
Sum of diagonlas: 12
```

