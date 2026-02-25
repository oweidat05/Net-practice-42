# Level 7 – Packets Travel Hop by Hop

## 🖼️ Network Diagram
![Level 7 Diagram](../diagrams/level7.jpg)
## 📘 Overview

This example demonstrates how packets travel across multiple routers to reach their destination.

A device does not need to know the entire network path.  
It only needs to know the next hop.  
Each router then forwards the packet to the next router until it reaches the final host.

---

## 🟢 Host Role

Host A sends traffic to its default gateway.  
It does not know the full route to Host C.

The host only knows:
- Its own network  
- Its gateway  

---

## 🔵 Router Role

Routers forward packets step by step.

- Router 1 receives the packet from Host A  
- Router 1 forwards it to Router 2  
- Router 2 forwards it to Host C  

Each router decides the next hop using its routing table.

---

##  What Happens

1. Host A sends the packet to its gateway  
2. Router 1 checks its routing table  
3. Router 1 forwards the packet to Router 2  
4. Router 2 forwards the packet to Host C  

The packet reaches the destination hop by hop.

---
