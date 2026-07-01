---
title: Day 12 of 100 Days of Python
date: 2026-07-01 09:55:00 +00:00
description: Practising Dictionary
categories: Coding
tags: Python
---
Today is Day 12. I practised more programs based on the dictionary.

```python
# Write a program that looks at a string, counts the characters, and tells you which character appeared the most times total.
st = "Thisisastring"
a = {}
max = 0
most_frequent = ""

for ch in st:
    if ch in a:
        a[ch] += 1
    else:
        a[ch] = 1
print(a)
for ch in st:
    if a[ch]>max:
        max = a[ch]
        most_frequent = ch
print(f"Most frequent: {most_frequent} \nNo of times appeared: {max}")


```

Output:

```
{'T': 1, 'h': 1, 'i': 3, 's': 3, 'a': 1, 't': 1, 'r': 1, 'n': 1, 'g': 1}
Most frequent: i 
No of times appeared: 3
```

