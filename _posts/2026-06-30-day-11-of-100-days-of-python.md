---
title: Day 11 of 100 Days of Python
date: 2026-06-30 20:15:00 +00:00
description: Practising Matrix and Dictionary
categories: Coding
tags: Python
---
Today is June 30 and 11th Day. I practised Tranpose Matrix in Python.

```python
# Transpose Matrix
m = [
    [1, 2, 3],
    [4, 5, 6]
]
r = len(m)
c = len(m[0])
r2, c2 = c, r

# FIX: Build a grid where every single row is completely independent in memory
b = []
for i in range(0, r2):
    b.append([0] * c2)

# Your loop logic here is 100% PERFECT!
for i in range(0, r2):
    for j in range(0, c2):
        b[i][j] = m[j][i]

# Print out the final matrix line by line
print("Transposed Matrix:")
for i in range(0, r2):
    print(b[i])  # Changed from b[0] to b[i] to print each distinct row

```

I have also started learning Dictionary in Python. It is very easy to understand and by using it, the programes based on lists become easier.

![image.png](assets/img/image-20.png)

```python
# Write a program that takes a string of text and counts exactly how many times each individual character appears, storing the results in a dictionary.
txt = "success"
f = {}
for ch in txt:
    if ch in f:
        f[ch] += 1
    else:
        f[ch] = 1
print(f"Frequency of each character: {f}")
```

Output:

```
Frequency of each character: {'s': 3, 'u': 1, 'c': 2, 'e': 1}
```

