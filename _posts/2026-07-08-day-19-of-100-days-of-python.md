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
s=0;
for key in user_keys:
    for i in key:
        s = s+ ord(i)
    ti = s%underlying_array_size
    print(f"Key '{key}' maps to array index: {ti}")
```

Output:

```
Key 'alpha' maps to array index: 8
Key 'beta' maps to array index: 0
Key 'gamma' maps to array index: 5
Key 'delta' maps to array index: 7
```

