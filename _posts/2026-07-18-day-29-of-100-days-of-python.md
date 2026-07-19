---
title: Day 29 of 100 Days of Python
date: 2026-07-18 23:27:00 +00:00
description: Practising DSA
categories: Coding
tags: Python
---
Today I practised the Binary Search Tree.

```python
# Binary Search Tree

class Node:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right= None
def insert(root, key):
    if root is None:
        return Node(key)
    if key<root.value:
        root.left = insert(root.left, key)
    if key>root.value:
        root.right = insert(root.right, key)
    return root
root = None
root = insert(root, 50)
root = insert(root, 30)
root = insert(root, 70)

print("Root value:", root.value)
print("Left value:", root.left.value)
print("Right value:", root.right.value)
```

  
Output:

```
Root value: 50
Left value: 30
Right value: 70
```

