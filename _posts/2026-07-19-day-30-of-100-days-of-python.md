---
title: Day 30 of 100 Days of Python
date: 2026-07-19 23:22:00 +00:00
description: Practising DSA
categories: Coding
tags: Python
---
Today I revised recursion.

I practised simple recursive function to count number in reverse from 10 to 0, with n==0 being base case and stopping further calling of function.

```python
# Recursion

def countdown(n):

    if n==0:
        print("0")
        return
    print(f"number: {n}")

    countdown(n-1)

countdown(10)
```

Output:

```
number: 10
number: 9
number: 8
number: 7
number: 6
number: 5
number: 4
number: 3
number: 2
number: 1
0
```

