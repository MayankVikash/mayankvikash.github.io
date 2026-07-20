---
title: Day 31 of 100 Days of Python
date: 2026-07-20 22:48:00 +00:00
description: Practising DSA
categories: Coding
tags: Python
---
Today i practised simple recursion.

```python
def sum_to_n(n):
    if n==1:
        return 1
    return n + sum_to_n(n-1)
result =sum_to_n(5)
print(result)
```

