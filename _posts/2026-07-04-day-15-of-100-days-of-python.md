---
title: Day 15 of 100 Days of Python
date: 2026-07-04 13:21:00 +00:00
description: Practising Reading and Writing Files in Python
categories: Coding
tags: Python
---
Today, I started learning to read and write files in Python with open(). I practised two questions today.

The first problem was basic reading and writing files in Python, and also using a for loop.

```python
with open("quest_log.txt", "w") as file:
    file.write("Quest: Kill the Dragon\n")
    file.write("Status: In Progress\n")
    file.write("Reward: 5000 Gold\n")
with open("quest_log.txt", "r") as file:
    content = file.read()
    print(content)
with open("quest_log.txt", "a") as file:
    file.write("Bonus: +1000 EXP\n")
with open("quest_log.txt", "a") as file:
    file.write("Location: Asgard Mountains\n")
with open("quest_log.txt", "r") as file:
    for line in file:
        print(line.strip())
```

I also learned the strip() method of strings and how to append files without completely rewriting them while solving this problem. 

The second question used conditional statements. It became a little tricky, but I was able to solve it.

```python
# Write a script that reads a simulated server log file, filters out specific high-priority security warnings, and writes only those filtered threats into a completely separate output file.

logs = [
    "INFO: User login successful\n",
    "WARN: High CPU usage detected\n",
    "CRITICAL: Unauthorized access attempt\n",
    "INFO: Database backup completed\n",
    "CRITICAL: Database connection lost\n"
]
with open("server_log.txt", "w") as file:
    file.writelines(logs)
with open("server_log.txt", "r") as infile, open("threats.txt", "w") as outfile:
    for line in infile:
        if "CRITICAL" in line:
            outfile.write(line)
with open("threats.txt", "r") as file:
    print(file.read())
```

  
Output for the second question:

CRITICAL: Unauthorized access attempt

CRITICAL: Database connection lost



&nbsp;