---
title: Day 2 of 100 Days of Python
date: 2026-06-21 21:03:00 +00:00
description: Practising Number manipulation in Python
categories: Coding
tags: Python
---
Today is Day 2 of my 100 Days of Python Challenge. Yesterday, I learned about the Conditional Statements like if, else and elif, which are used to execute a block of code if the required conditions are met.

 Using these, I solved two incredibly common coding questions that are asked in the exams.

Today's goal is to solve some number manipulation questions in Python to brush up on my coding knowledge. The first program is very simple. It basically inputs (asks for a 3-digit number) a three-digit number. Then, using division and modulo operations to extract the digit into 3 different variables, without using loops. And finally, adds the digits, stores and prints the summation of its digits. 

While writing this program, I learned that using // means that only the integer division takes place (ex. 5//2 = 2 and 5/2 = 2.5).

![](assets/img/image-5.png)



```python
# number manipulation in python
# Digit Extraction and sum of digit of a 3-digit number
n = int(input("Enter a number of 3 digit"))
d1 = n //100
#  '//' for integer division, ex- 5//2 = 2 instead of 2.5
d2 = (n//10)%10
d3 = n%10

dsum = d1 +d2 +d3

print(f"The digits are: {d1}, {d2}, and {d3}")
print(f"Sum of 3 digits: {dsum}")
```

The second program uses a while loop to reverse the input number. And checks for a palindrome number. When a reversed number is equal to the original number, it is called a palindrome number. I will focus more on these types of questions starting tomorrow. 

![image.png](assets/img/image-6.png)

```python
# Take an integer input, reverse it mathematically, and determine if it's a palindrome
# palindrome is number equal to its reversed like 99 and 88 or 121
n = int(input("Enter a number to check for palindrome"))
og = n
rn = 0
while n>0:
    d = n%10
    rn = (rn*10) + d
    n = n//10
print(rn)
if og==rn:
    print("It is palindrome")
else:
    print("It is not")
```

Learned the while loop and how to reverse a number using a loop and an extra variable.

```python
rn = (rn*10) + d
```

The original value of rn is 0. During the first iteration, 0*10 + d = 0 + d = d. In the second iteration, rn = d*10 + d. Since the value of d changes to the last digit of the number after it is divided by 10, the final value of rn is the reverse of the original number.

ex - 145

1st loop: d = 5, rn = 0 + d = 5, n = 145//10 = 14

2nd loop: d = 4, rn = 5 * 10 + d = 54, n = 14//10 = 1

3rd loop: d = 1, rn = 54 * 10 + d = 541, n = 1//10 = 0

After the third loop, the condition n>0 is not true. So the loop stops, and the final value of rn is 541, which is the reverse and palindrome of 145.