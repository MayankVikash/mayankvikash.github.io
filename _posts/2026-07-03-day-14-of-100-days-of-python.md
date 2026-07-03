---
title: Day 14 of 100 Days of Python
date: 2026-07-03 09:35:00 +00:00
description: Practising Functions
categories: Coding
tags: Python
---
Today is Day 14/100. I am practising problems based on Python Functions. 

Write a function called withdraw_money that safely processes a bank withdrawal. It must check for invalid amounts and insufficient funds using guard clauses and use a default daily transaction fee if none is specified.

```python
def withdraw(balance, amt, fee =25):
    if amt<=0:
        return "Invalid Amount"
    if amt + fee > balance:
        return "Insufficient Funds"
    balance = balance - (amt +fee)
    return f"Withdrawal successful. New balance: {balance}"

print(withdraw(5000, -100))     # Should trigger Guard Clause 1
print(withdraw(5000, 6000))     # Should trigger Guard Clause 2 (using default 25 fee)
print(withdraw(5000, 1000, 50)) # Valid withdrawal, overriding fee to 50 
```

Output for problem 1:

```
Invalid Amount
Insufficient Funds
Withdrawal successful. New balance: 3950
```

This is the second question of the day. Here, I calculated min, max and avg values inside a function and returned them as a tuple.

```python
# Write a function called analyze_scores that takes a list of numbers (representing exam marks or test scores) and returns three distinct metrics at the exact same time: the Minimum score, the Maximum score, and the Average score.
def analyze_score(marks):
    min =marks[0]; max= 0; s=0;
    for i in range(0,l):
        if marks[i]>max:
            max = marks[i]
        if marks[i]<min:
            min = marks[i]
        s = s+marks[i]

    avg = s//l
    return max,min,avg
mark = [85, 92, 78, 99, 64, 88]
l = len(mark)
r = analyze_score(mark)
highest = r[0]
lowest = r[1]
average = r[2]
print(f"Highes: {highest}, lowest: {lowest}, avg: {average}")
```

Output of program 2:

```
Highes: 99, lowest: 64, avg: 84
```

