---
title: Day 1 of 100 Days of Python
date: 2026-06-21 00:31:00 +00:00
description: Practising simple Python programs on first day of challenge
categories: Coding
tags: Python
---
Today is the first day of the coding challenge I took (although by the time I finish writing this post, it will be past 12 in the morning).

Yesterday, I played around with basic Python syntax, such as print, which lets us display text in the console. Today, my goal is to learn more about basic Python syntax and work through a few practice questions. 

![SC1](assets/img/image-3.png)

This was one problem that I solved yesterday. These kinds of questions are asked repeatedly in board exams, and I am very familiar with them. I will do more of these kinds of questions tomorrow.

```python
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



This is the second program:

![image.png](assets/img/image-4.png)

It is also one of the most asked types of questions in the board exam.

Here is the code

```python
# Input the basic salary of an employee. Compute the Gross Salary and Net Salary based on the following:
# HRA (House Rent Allowance) = 20% of Basic
# DA (Dearness Allowance) = 50% of Basic
# Gross Salary = Basic + HRA + DA
# Tax Deduction: If Gross Salary is over ₹1,00,000, deduct 10% of Gross as tax; otherwise, tax is 0.
# Net Salary = Gross Salary - Tax Deduction


bs = int(input("Enter basic salary"))
hra = 0.2 * bs
da = 0.5*bs
gross = bs + hra + da
tax = 0.0

if gross>100000:
    tax = 0.1*gross
else:
    tax = 0.0
net = gross - tax

print(f"Basic Salary: {bs}")
print(f"hra: {hra}")
print(f"da: {da}")
print(f"tax: {tax}")
print(f"net salary: {net}")
```

After practising these programs, I am familiar with the input syntax of Python as well as Conditional Statements. For Tomorrow, I plan to practise some number manipulation exercises.