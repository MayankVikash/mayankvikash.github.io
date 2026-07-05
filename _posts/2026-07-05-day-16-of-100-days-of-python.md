---
title: Day 16 of 100 Days of Python
date: 2026-07-05 20:33:00 +00:00
description: Learning Class and Objects
categories: Coding
tags: Python
---
Today on Day 16, I started Classes and Objects in Python. This is the beginner program I tried to get familiar with writing classes.

```python
class Character:
    def __init__(self, name, level, power):
        self.name =name
        self.level =level
        self.power = power 
    def profile(self):
        print(f"Character: {self.name} | Level: {self.level} | Power Type: {self.power}")
player1 = Character("Alex", 50, "Telekinesis")
player1.profile()
```



&nbsp;