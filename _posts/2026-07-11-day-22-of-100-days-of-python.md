---
title: Day 22 of 100 Days of Python
date: 2026-07-11 22:55:00 +00:00
description: Practising DSA
categories: Coding
tags: Python
---
Today i practised Linked List while using a separate class for linking Nodes.

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
class LinkedList:
    def __init__(self):
        self.head =None
    def prepend(self,data):
        new_node = Node(data)
        new_node.next = self.head
        self.head = new_node
    def display(self):
        current = self.head
        while current is not None:
            print(current.data, end=" -> ")
            current = current.next
        print("None")
ll = LinkedList()
ll.prepend(30)
ll.prepend(20)
ll.prepend(10)
ll.display()

# Expected Output: 10 -> 20 -> 30 -> None
```

Output:

```
10 -> 20 -> 30 -> None
```

