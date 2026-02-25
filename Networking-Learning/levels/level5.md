
# Level 5 – Specific Routes vs Default Gateway

## 🖼️ Network Diagram
![Routing Decision Diagram](../diagrams/level5.png)

## 📘 Overview

This example introduces the concept of routing decisions.  
A device may know multiple possible paths to send traffic, and it must choose the correct one.

When a destination network is explicitly known, the device uses a specific route.  
If no matching route exists, it falls back to the default gateway.

---

## 🟢 Known Network Route

If Host A wants to reach a network that is explicitly defined in its routing table, it sends packets through that specific route.

For example, if a route exists for:


172.16.0.0/16


then traffic to that network will follow the defined path.

---

## 🔵 Default Gateway Role

If the destination network does not match any known route, the device sends traffic to the default gateway.

The default route acts as the “last option” for unknown destinations.

---

##  Routing Decision Order

Devices choose routes in this order:

1. Directly connected network  
2. Specific route in the routing table  
3. Default gateway  

This ensures traffic always follows the most precise path.

---
