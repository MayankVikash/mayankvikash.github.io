---
title: Day 3 of 100 Days of Python
date: 2026-06-22 19:54:00 +00:00
description: Practising Number manipulation in Python
categories: Coding
tags: Python
---
Today is June 22nd, the third day of the 100 Days of Python Coding challenge. I am doing some Number Manipulation questions in Python that use a while loop and digit extraction.

The first program is to check for an Armstrong Number. To solve it, I use a while loop and a counter variable to get the number of digits in the input number. Then, with another loop, I use the while loop again, but this time extract a digit, raise it to the power of its number of digits and then add their sum in a separate variable 's'.

![image.png](assets/img/image-7.png)



```python
# Armstrong Number. An Armstrong number (like 153 or 371) is a number equal to the sum of its own digits raised to the power of the number of digits
n = int(input("Enter a number to check for Armstrong Number"))
p = n
s=0
c = 0
while n>0:
    c=c+1
    n = n//10
n = p
while n>0:
    d = n%10
    print(f"Current digit: {d}")
    s = d**c + s
    print(f"Current sum: {s}")
    n = n//10
print(f"No. of digits: {c}")
print(f"Sum of digit raised to number of digit: {s}")
if s==p:
    print("It is Armstrong Number")
else:
    print("It is not")
```

I learned that in Python, instead of Math.pow, we use double asterisk (**) to raise a number to a power. 

I also discovered another method for calculating the number of digits in an input number. It is that we can use this syntax, `len(str(num))` which converts the number into a string and calculates its length.

