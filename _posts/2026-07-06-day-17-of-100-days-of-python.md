---
title: Day 17 of 100 Days of Python
date: 2026-07-06 12:47:00 +00:00
description: Learning Object Oriented Programming
categories: Coding
tags: Python
---
I had been trying to solve this question since last night. Today, I was able to solve it, after I removed a list intialization from the function code block to **init** function.

```python
# Create two classes where one class instantiates single objects, and the second class acts as a central repository that filters those objects based on a specific property threshold.

class ServerNode:
    def __init__(self, node_id, active_connections):
        self.node_id = node_id
        self.active_connections = active_connections
class ClusterManager:
    def __init__(self):
        self.nodes = []
        self.nid = []
        self.nsc = []
    def register_node(self, node_object):
        self.nob = node_object

        self.nid.append(self.nob.node_id)
        self.nsc.append(self.nob.active_connections)
        self.nodes.append(self.nid)
        # print(f"Self nob: {self.nid}, active conn: {self.nsc[0]}")
    def get_overloaded_nodes(self, threshold):
        self.threshold = threshold
        rl = []
        counterv =0
        for i in self.nid:
            if self.nsc[counterv] > self.threshold:
                rl.append(self.nid[counterv])
            counterv+=1
        return rl

manager = ClusterManager()
manager.register_node(ServerNode("Node-A", 120))
manager.register_node(ServerNode("Node-B", 45))
manager.register_node(ServerNode("Node-C", 200))

print(manager.get_overloaded_nodes(100))
```

Output for Program 1:

```
['Node-A', 'Node-C']
```

The second program I made is:

```python
# Create a parent class that handles core transaction attributes and a child class that inherits those attributes while adding conditional validation logic specific to specialized accounts.

class BaseTransaction:
    def __init__(self, transaction_id, amount):
        self.transaction_id=transaction_id
        self.amount=amount
class AuthorizedTransaction(BaseTransaction):

    def __init__(self,transaction_id,amount, security_token):
        super().__init__(transaction_id,amount)
        self.security_token = str(security_token)
    def process_transaction(self):
        if self.security_token == "AUTH_VALID":
            return f"Transaction {self.transaction_id} processed for {self.amount}"
        else:
            return "Transaction Denied: Invalid Toekn"
t1 = AuthorizedTransaction("TXN-101", 5000, "AUTH_VALID")
t2 = AuthorizedTransaction("TXN-102", 750, "AUTH_FAILED")

print(t1.process_transaction())
# Expected Output: Transaction TXN-101 processed for 5000

print(t2.process_transaction())
# Expected Output: Transaction denied: Invalid token


```

Output:

```
Transaction TXN-101 processed for 5000
Transaction Denied: Invalid Toekn
```

