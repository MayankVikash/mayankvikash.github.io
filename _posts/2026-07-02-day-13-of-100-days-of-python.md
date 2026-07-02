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

