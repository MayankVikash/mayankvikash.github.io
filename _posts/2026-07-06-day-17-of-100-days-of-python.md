---
title: Day 17 of 100 Days of Python
date: 2026-07-06 12:47:00 +00:00
description: Learning Object Oriented Programming
categories: Coding
tags: Python
---
I had been trying to solve this question since last night. Today, I was able to solve it, after I removed a list intialization from the function code block to __init__ function.

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

