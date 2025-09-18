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
```
### 2️⃣ Create DHCP Pool
```bash
R1(config)# ip dhcp pool Nour
R1(dhcp-config)# network 192.168.1.0 255.255.255.0
R1(dhcp-config)# default-router 192.168.1.1
R1(dhcp-config)# dns-server 8.8.8.8
```
### 3️⃣ Connect Devices
- Connect PCs to the switch.
- Connect the switch to the router.
### 4️⃣ Set PCs to DHCP Mode
- Go to each PC → Desktop → IP Configuration → Select DHCP.
- Verify IP, Gateway, and DNS are assigned correctly.
---
### 🖼️ Lab Topology Screenshot
![1754571266152](https://github.com/user-attachments/assets/e1c83b0e-3593-43fd-8d6d-d21f812d7f93)


