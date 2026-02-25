# Level 10 – End-to-End Routing Across a Complex Network

## 🖼️ Network Diagram
![Level 10 Diagram](../diagrams/level10.jpg)
## 📘 Overview

This level represents a complete real-world routing scenario.

Multiple hosts, subnets, routers, and routing tables interact together to deliver packets across the network.  
Communication only succeeds when every device makes the correct routing decision.

---

## 🟢 Host Responsibilities

Each host must:

- Use the correct subnet mask
- Identify when the destination is outside its network
- Send traffic to the proper default gateway

If the gateway is incorrect, communication fails immediately.

---

## 🔵 Router Responsibilities

Each router must:

1. Check its directly connected networks  
2. Select the most specific matching route  
3. Use a default route only when no better match exists  
4. Forward the packet to the correct next hop  

Routing decisions are made independently at each router.

---

##  Packet Journey

1. Source host sends traffic to its gateway  
2. First router selects the best route  
3. Packet is forwarded to another router if needed  
4. Final router forwards the packet to the destination subnet  
5. Destination host receives the packet  

Every hop must be correct for the communication to succeed.

---

## 💡 What This Level Teaches

- Real networks involve multiple routing decisions  
- Hosts only know their gateway, not the full path  
- Routers independently choose the best route  
- Longest Prefix Match applies at every step  
- Default routes are fallback paths  
- A single misconfiguration can break the entire path
