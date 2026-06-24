---
title: Day 5 of 100 Days of Python
date: 2026-06-24 21:42:00 +00:00
description: Practising String Manipulation
categories: Coding
tags: Python
---
Today, I solved a program on String Manipulation.

![image.png](assets/img/image-11.png)

The question was to input a sentence and print individual words in different lines as well as count the number of words.

```python
# Write a program that takes a complete sentence as input. Without using any built-in split or search functions, read the string character by character using a loop to:
# Print each individual word on its own line as soon as it is detected.
# Count and print the total number of words in that sentence

sen = input("Enter the sentence ")
cw = ""
wcount = 0

for ch in sen:
    if ch == " ":
        print(f"wORD: {cw}")
        wcount += 1
        cw = ""
    else:
        cw = cw + ch
if cw != "":
        print(f"Last word: {cw}")
        wcount += 1
print(f"Total word count: {wcount}")
```

