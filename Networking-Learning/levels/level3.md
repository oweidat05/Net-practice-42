# Level 3 – Same Switch Does Not Mean Same Network

## 🖼️ Network Diagram
![Switch Network Diagram](../diagrams/level3.png)

## 📘 Overview

This example shows three devices connected to the same switch.  
Although they share the same physical connection, communication still depends on whether they belong to the same subnet.

A switch operates at Layer 2 and does not change IP addressing rules.  
If devices are placed in different networks, they cannot communicate directly even if they are connected to the same switch.

---

## 🟢 Hosts on the Switch

- **Host A:** 192.168.20.10/24  
- **Host B:** 192.168.20.30/24  
- **Host C:** 192.168.21.5/24  

With a `/24` mask:


192.168.20.0/24


contains Host A and Host B.


192.168.21.0/24


contains Host C.

This means Host C is in a different network.

---

##  What Happens

Host A and Host B can communicate directly because they share the same subnet.

Host C cannot communicate with them directly, even though all devices are connected to the same switch.

A router would be required to forward packets between the two networks.

---
