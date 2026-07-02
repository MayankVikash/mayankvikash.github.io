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

![Screenshot](assets/img/image-21.png)

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

The third program checks the items in the dictionary and applies a 10% discount.

```python
# Write a feature that applies a 10% off discount to every single product inside the store's inventory list, updating the records in place.
store_items = [
    {"name": "Keyboard", "price": 1500},
    {"name": "Smartphone", "price": 45000},
    {"name": "Headphones", "price": 8000},
    {"name": "Gaming PC", "price": 120000},
    {"name": "USB Cable", "price": 500}
]
for items in store_items:
    items["price"] = int(items["price"] - (0.1 * items["price"]))
    print(f"{items["name"]} (Price: {items["price"]})")
```

Output:

```
Keyboard (Price: 1350)
Smartphone (Price: 40500)
Headphones (Price: 7200)
Gaming PC (Price: 108000)
USB Cable (Price: 450)
```

This is the question for the next problem: Write a program that looks at a company's expense records and calculates the total amount of money spent per department.

```python
# Write a program that looks at a company's expense records and calculates the total amount of money spent per department
expenses = [
    {"item": "Laptops", "amount": 150000, "dept": "IT"},
    {"item": "Chairs", "amount": 25000, "dept": "HR"},
    {"item": "Software Licenses", "amount": 45000, "dept": "IT"},
    {"item": "Desk Plants", "amount": 5000, "dept": "HR"},
    {"item": "Cloud Hosting", "amount": 80000, "dept": "IT"},
    {"item": "Recruiting Ads", "amount": 35000, "dept": "HR"}
]

dept_total= {}


for items in expenses:
    if items["dept"] in dept_total:
        dept_total[items["dept"]] = dept_total[items["dept"]] + items["amount"]
    else:
        dept_total[items["dept"]] = items["amount"]

print(dept_total)

```

Output:

```
{'IT': 275000, 'HR': 65000}
```

