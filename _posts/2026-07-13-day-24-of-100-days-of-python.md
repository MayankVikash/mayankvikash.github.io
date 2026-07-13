---
title: Day 24 of 100 Days of Python
date: 2026-07-13 19:33:00 +00:00
description: Practising DSA
categories: Coding
tags: Python
---
Today is Day 24. I practised Stack Data Structures today. It follows Last in First Out (LIFO) principle. I used the Python Lists and its built in functions to get idea of how Stack works. I used .append() function to add a value in the end of the list and .pop() function to get the last index value and also remove it from the list. Here is the code:

```python
# Stack
history_stack = []
history_stack.append("google.com")
history_stack.append("wikipedia.org")
history_stack.append("github.com")
print(history_stack)

back_page= history_stack.pop()
print(f"Clicked back. Leaving {back_page}")
print(history_stack)
```

Output for Program 1:

```
['google.com', 'wikipedia.org', 'github.com']
Clicked back. Leaving github.com
['google.com', 'wikipedia.org']
```

