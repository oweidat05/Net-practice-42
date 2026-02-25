
# Level 4 – Communication Between Networks Requires a Router

## 🖼️ Network Diagram
![Level 4 Diagram](../diagrams/level4.jpg)
## 📘 Overview

This example introduces the concept of routing between networks.

Even though devices may be physically connected through a switch, communication between different networks requires a router.  
The router acts as a gateway that forwards packets from one network to another.

---

## 🟢 Local Network (LAN)

- **Host A:** 192.168.10.10/28  
- **Host B:** 192.168.10.20/28  

With a `/28` mask, the network becomes:


192.168.10.0/28


Devices inside this network can communicate directly.

---

## 🔵 Router Role

The router connects this LAN to another network using its interfaces:

- **Router LAN Interface:** 192.168.10.1/28  
- **Router WAN Interface:** 172.16.0.1/24  

The router serves as the gateway for devices in the LAN.

---

##  What Happens

If Host A wants to communicate with another network, it must send packets to the router.  
The router then forwards the packets to the correct destination network.

Without a gateway, devices cannot reach networks outside their local subnet.

---
