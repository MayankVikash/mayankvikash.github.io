---
title: Day 13 of 100 Days of Python
date: 2026-07-02 10:07:00 +00:00
description: Practising Dictionary
categories: Coding
tags: Python
---
Today is 2nd July (Day 13)

```python
# Write a program that manages an electronic store inventory and calculates the total financial value of all the stock combined inside the shop.
inventory = [
    {"name": "Laptop", "price": 50000, "quantity": 4},
    {"name": "Mouse", "price": 1200, "quantity": 10},
    {"name": "Monitor", "price": 15000, "quantity": 2}
]
totalv = 0

for item in inventory:
    print(f"For {item["name"]}, the price is {item["price"]} and quantity is {item["quantity"]}. Total Item value: {item["price"]*item["quantity"]}")
    totalv = totalv+ item["price"]*item["quantity"]
print(f"Total stock: {totalv}")
```

Output:

```python
For Laptop, the price is 50000 and quantity is 4. Total Item value: 200000
For Mouse, the price is 1200 and quantity is 10. Total Item value: 12000
For Monitor, the price is 15000 and quantity is 2. Total Item value: 30000
Total stock: 242000
```

Here is the second Program. It uses if statements along with lists and dictionaries.

![image.png](blob:https:/app.pagescms.org/84a2f1c3-8369-402e-ab8a-4fdf78336602)

```python
# Write a system feature that filters out and displays only the "Premium" products from an expanded inventory list—meaning any item that costs more than 10,000.
store_items = [
    {"name": "Keyboard", "price": 1500},
    {"name": "Smartphone", "price": 45000},
    {"name": "Headphones", "price": 8000},
    {"name": "Gaming PC", "price": 120000},
    {"name": "USB Cable", "price": 500}
]
premium_items = []
for items in store_items:
    if items["price"]>10000:
        premium_items.append(items)
print(premium_items)
print("Premium List:")
for pitems in premium_items:
    print(f"- {pitems["name"]} (Price: {pitems["price"]})")
```

Output:

```
[{'name': 'Smartphone', 'price': 45000}, {'name': 'Gaming PC', 'price': 120000}]
Premium List:
- Smartphone (Price: 45000)
- Gaming PC (Price: 120000)
```

