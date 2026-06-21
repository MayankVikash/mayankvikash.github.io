---
layout: post
title: Day 1 of 100 Days of Python
date: 2026-06-21 00:31:00 +00:00
description: Practising simple Python programs on first day of challenge
categories: Coding
tags: Python
---
Today is the first day of the coding challenge I took (although by the time I finish writing this post, it will be past 12 in the morning).

Yesterday, I played around with the basic Python syntax, like print, which allows us to display text in the console. Today, my goal is to learn more about basic Python syntax and practice a few questions. 

![SC1](assets/img/image-3.png)

This was one problem that I solved yesterday. These kinds of questions are asked repeatedly in board exams, and I am very familiar with them. I will do more of these kinds of questions tomorrow.

```
#Electricity Bill question in Python

# An electricity board charges for electricity delivered to domestic consumers based on the number of units consumed.

# For the first 100 units: ₹4.00 per unit

# For the next 200 units: ₹6.00 per unit

# Beyond 300 units: ₹8.00 per unit

# A fixed meter charge of ₹200 is added to every bill.

# Given the units consumed, calculate the total bill.

units = int(input("Enter units consumed"))
fixc = 200
amt = 0.0
if units <=100:
    amt = 4.00*units
elif units <= 300:
    amt = (100*4.00) + ((units -100)*6.00)
else:
    amt = (100*4.00) + (200*6.00) + ((units-300)*8.00)
tbill = amt + fixc
print(f"Total amount to be paid: {tbill}")
```

