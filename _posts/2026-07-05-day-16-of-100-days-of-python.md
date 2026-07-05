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

I solved a few other programs also to get familiar with the syntax of constructors.

```python
class EmployeeProfile:
    def __init__(self,emp_id,name,depart):
        self.emp_id = emp_id
        self.name= name
        self.depart = depart

    def fetch_details(self):
        return f"EmpID: {self.emp_id} | Name: {self.name} | Dept: {self.depart}"
emp1 = EmployeeProfile("E1154", "Alex", "IT")
x = emp1.fetch_details()
print(x)

```

Program 3:

```python
class InventoryItem:
    def __init__(self, it_id, it_name, sc):
        self.it_id = it_id
        self.it_name = it_name
        self.sc = sc
    def up_st(self, amt):
        if amt<0:
            if -1*amt > self.sc:
                return "Insufficient stock"
        self.sc += amt
        return f"New stock: {self.sc}"
item = InventoryItem("SK81333", "Lights" , 50)
x = item.up_st(-145)
print(x)
```

Output for program 3:

```
New stock: 35 (for amt = 15)
New stock: 5 (for amt = -45)
Insufficient stock (for amt = -145)
```

Program 4: Create a class that models a system tracking a sequence of measurements, allowing updates to the data and reporting calculations based on its internal state.

```python
class DataTracker:
    def __init__(self):
        self.records = []
    def add_record(self, value):
        self.records.append(value)
    def get_variance(self):
        l = len(self.records)
        if len(self.records) < 2:
            return 0.0
        else:
            variance = 0.0
            s=0

            for num in self.records:
                s = s + num
            mean = s//l
            for i in (0,len(self.records)):
                variance = (variance + (i-mean)**2)/l
            return variance
tracker = DataTracker()
tracker.add_record(10)
tracker.add_record(20)
tracker.add_record(30)
x = tracker.get_variance()
print(x)
```

Output:

```
140.7777777777778
```

