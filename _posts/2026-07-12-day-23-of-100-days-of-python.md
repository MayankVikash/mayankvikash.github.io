---
title: Day 23 of 100 Days of Python
date: 2026-07-12 23:18:00 +00:00
description: Practising DSA
categories: Coding
tags: Python
---
Practising Linked List

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
class LinkedList:
    def __init__(self):
        self.head = None
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
    def append(self, data):
        new_node = Node(data)
        if self.head is None:
            self.head = new_node
            return
        
        current = self.head
        while current.next is not None:
            current = current.next
        current.next = new_node
ll = LinkedList()
ll.append(10)
ll.append(20)
ll.prepend(5)
ll.append(30)
ll.display()

# Expected Output: 5 -> 10 -> 20 -> 30 -> None
```

Output:

```
5 -> 10 -> 20 -> 30 -> None
```

