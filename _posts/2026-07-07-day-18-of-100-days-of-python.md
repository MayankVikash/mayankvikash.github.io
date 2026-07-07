---
title: Day 18 of 100 Days of Python
date: 2026-07-07 10:38:00 +00:00
description: Practising Object Oriented Programming (Inheritance and Overiding)
categories: Coding
tags: Python
---
The first program I did today was to first declare a parent class, which simply returns a float value. After that, inherit the parent class into a subclass and override the function and return the total cost after calculating the tax rate.

```python
# Create a baseline system component class and a specialized child class that overrides a foundational status method to include specific calculations.

class SystemComponenet:
    def __init__(self, component_name, base_cost):
        self.component_name= component_name
        self.base_cost = base_cost
    def get_total_cost(self):
        return float(self.base_cost)
class TaxedComponent(SystemComponenet):
    def __init__(self, component_name, base_cost, tax_rate):
        super().__init__(component_name, base_cost)
        self.tax_rate = tax_rate
    def get_total_cost(self):
        return self.base_cost * (1+ self.tax_rate)
comp1 = SystemComponenet("Server Rack", 15000)
comp2 = TaxedComponent("GPU Cluster", 50000, 0.18)

print(comp1.get_total_cost())
print(comp2.get_total_cost())
```

Output for Program 1:

```
15000.0
59000.0
```

The second program I did today was try-except.

```python
# try:
#     result = 10/0
# except ZeroDivisionError:
#     print("Cannot divide by 0")
#     result =0
# print(result)

# Create a data cleaning utility function that attempts to normalize input values into a uniform numerical format while defending against malformed data types.


def normalize_reading(data_input):
    try:
        result = float(data_input)
    except ValueError:
        result = 0.0
        return(result)
print(normalize_reading("14.5"))
print(normalize_reading("N/A"))


```

Output:

```
None
0.0
```

