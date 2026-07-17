---
title: Day 28 of 100 Days of Python
date: 2026-07-17 22:38:00 +00:00
description: Practising DSA
categories: Coding
tags: Python
---
I started Binary Tree today. It is a data structure where the top value of the tree is called Root. Its left side value is supposed to be smaller than root while the right side larger.

I made a Binary Tree structure in Python using Class.

```python
# Binary Tree
class Node:
    def __init__(self, key):
        self.val = key
        self.left = None
        self.right = None
root = Node(50)
root.left = Node(30)
root.right = Node(70)

print("Root value ", root.val)
print("Left value ", root.left.val)
print("Right value ", root.right.val)
```

Output

```
Root value  50
Left value  30
Right value  70
```

