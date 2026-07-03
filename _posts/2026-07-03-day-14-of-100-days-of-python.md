---
title: Day 14 of 100 Days of Python
date: 2026-07-03 09:35:00 +00:00
description: Practising Functions
categories: Coding
tags: Python
---
Today is Day 14/100. I am practising problems based on Python Functions.

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

