---
title: Day 6 of 100 Days of Python
date: 2026-06-25 22:10:00 +00:00
description: Creating a Shopping Cart with loop and lists
categories: Coding
tags: Python
---
![image.png](assets/img/image-13.png)

Today, I created a shopping cart with lists and an infinite while loop. I also used list methods like append and len().

```python
# Write a program that manages a user's shopping cart using loops and lists.
# Allow the user to input items one by one.
# If they type the word "checkout", the input loop stops.
# If they enter an item that already exists in their cart list, do not add it again. Instead, print a message saying "Item already in cart".
# At checkout, print the final organized product list and the total number of unique items ready for shipment.


cart = []
print("Enter cart items. Enter 'checkout' to print the final cart")
while True:
    product = input("Enter product name ")
    if product.lower() == 'checkout':
        break
    if product in cart:
        print(f"{product} is already in cart")
    else:
        cart.append(product)
        print(f"{product} has been added to cart")

print(f"Total no. of items: {len(cart)}")
print("Items:")

for item in cart:
    print(f"={item}")
```

