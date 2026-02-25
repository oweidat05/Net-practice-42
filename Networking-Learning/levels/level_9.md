# Level 9 – Routing Across Multiple Networks

## 🖼️ Network Diagram
![Multi-Network Routing](../diagrams/level9.png)

## 📘 Overview

This example combines all previous routing concepts into one scenario.

Packets may travel across multiple routers before reaching their destination.  
Each router independently decides where to send the packet next based on its routing table.

The path is not decided once — it is decided at every hop.

---

## 🟢 Host Perspective

A host only knows:
- Its own subnet  
- Its default gateway  

It sends packets to the gateway when the destination is outside its local network.

---

## 🔵 Router Perspective

Each router checks its routing table and selects the best match:

1. Directly connected network  
2. Most specific matching route  
3. Default route if nothing else matches  

The router then forwards the packet to the next hop.

---

##  What Happens

1. Host A sends traffic to its gateway  
2. Router 1 checks its routing table  
3. Router 1 forwards to Router 2  
4. Router 2 performs its own routing decision  
5. Router 2 forwards to the destination network  

The packet reaches the destination hop by hop.

---
