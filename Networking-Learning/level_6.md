# Level 6 – Hosts Use a Gateway, Routers Know the Path

## 🖼️ Network Diagram
![Routing Through Gateway](../diagrams/level6.png)

## 📘 Overview

This example explains how a host reaches a remote network through a router.

A host does not need to know the full path to a destination.  
It only needs to know its default gateway.  
The router then uses its routing table to forward packets to the correct network.

---

## 🟢 Host Role

Host A is inside a local network:

- **Host A:** 192.168.1.10/24  
- **Default Gateway:** 192.168.1.1  

If the destination is outside the local subnet, the host sends packets to its gateway.

The host does not know where the final network is located.

---

## 🔵 Router Role

The router connects multiple networks:

- **LAN Interface:** 192.168.1.1/24  
- **WAN Interface:** 10.0.0.1/8  

The router contains routing information that tells it where to send packets next.

---

##  What Happens

1. Host A wants to reach a remote network  
2. It sends packets to the default gateway  
3. The router checks its routing table  
4. The router forwards packets to the correct network  

---
