# 🛠️ Router-DHCP-IP-Gateway-DNS Lab

## 🎯 Objective
This lab demonstrates how to configure a Cisco router to automatically assign:
- IP addresses
- Default gateway
- DNS settings  
to connected devices using DHCP in Cisco Packet Tracer.

---

## 💻 Lab Components
- 🛜 1 Router (R1)
- ♻️ 1 Switch (S1)
- 🖥️ 3 PCs (PC1, PC2, PC3)

---

## ⚙️ Configuration Steps

### 1️⃣ Configure Router Interface
```bash
R1> enable
R1# config t
R1(config)# interface gig0/0
R1(config-if)# ip address 192.168.1.1 255.255.255.0
R1(config-if)# no shutdown
