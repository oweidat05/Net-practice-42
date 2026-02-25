# Level 2 – The Subnet Mask Defines the Network Boundary

## 🖼️ Network Diagram
![Level 2 Diagram](../diagrams/level2.jpg)
## 📘 Overview

This example demonstrates two independent local networks.  
Even when devices are directly connected, communication depends on the subnet mask, not only on how close the IP addresses look.

The subnet mask defines the actual network boundary and determines whether devices belong to the same network.

---

## 🟢 Network 1 – LAN 1

- **Host A:** 192.168.50.10/27  
- **Host B:** 192.168.50.20/27  

With a `/27` subnet mask, the network becomes:


192.168.50.0/27


Both devices fall inside this network range, so they can communicate directly without a router.

---

## 🔵 Network 2 – LAN 2

- **Host C:** 10.0.0.1/30  
- **Host D:** 10.0.0.2/30  

With a `/30` mask, the network becomes:


10.0.0.0/30


Since both devices belong to the same network, they can also communicate directly.

---

## Key Rule

The subnet mask defines the network boundary, not just the IP address.

Two devices can communicate directly only if the subnet mask places them inside the same network.  
If the mask separates them into different networks, a router is required.

---



