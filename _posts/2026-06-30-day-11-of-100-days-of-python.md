---
title: Day 11 of 100 Days of Python
date: 2026-06-30 20:15:00 +00:00
description: Practising Matrix
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

