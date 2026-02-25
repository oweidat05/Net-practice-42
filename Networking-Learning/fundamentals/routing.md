# Routing Fundamentals

## 📘 What Is Routing?

Routing is the process of deciding how packets travel between networks.

When a device wants to communicate outside its subnet, it sends traffic to its **default gateway**.  
Routers then forward packets using routing tables until they reach the destination network.

Routing decisions happen at **every hop**, not once.

---

# 🧠 Host Routing Decision

A host follows this logic:

1. Compare destination IP with its subnet
2. If inside subnet → send directly
3. If outside subnet → send to default gateway

Hosts do not know full paths.  
They only know:

- their IP
- their subnet mask
- their gateway

---

# 🟢 Router Routing Table

Routers use a routing table:


Destination Network → Next Hop


Example:


192.168.10.0/24 → directly connected
10.0.0.0/8 → 192.168.1.1
0.0.0.0/0 → ISP Router


---

# 🔥 Router Decision Order (VERY IMPORTANT)

Routers choose routes in this order:

### 1️⃣ Directly Connected Network
If the destination is inside a connected interface → send directly.

---

### 2️⃣ Longest Prefix Match

If multiple routes match, choose the **most specific subnet**.

Example:


10.0.0.0/8
10.0.0.0/24


Destination: `10.0.0.5`

Router chooses:


10.0.0.0/24


because it is more specific.

---

### 3️⃣ Static or Learned Routes

If no direct match, router checks routing table entries.

---

### 4️⃣ Default Route

If nothing matches:


0.0.0.0/0


This acts as a fallback path.

Without a default route, unknown traffic is dropped.

---

# 🧩 Next Hop Concept

Routers do not send packets to the final destination directly.

They send to the **next hop**.

Example:


Destination: 172.16.0.10
Route: 172.16.0.0/16 → 10.0.0.2


Router forwards to `10.0.0.2`, not to the final host.

Each router repeats the same logic.

---

# 🔎 Routing Happens Hop by Hop

Path example:


Host → Gateway → Router1 → Router2 → Destination


Each device makes its own decision.

No device knows the full path.

---

# 💡 Key Routing Rules to Remember

- Hosts only know their gateway
- Routers know next hops, not full paths
- Longest prefix always wins
- Default route is fallback only
- Routing decisions happen at every hop

Routing is the backbone of how the Internet works.
