# 🛠️ Router-DHCP-IP-Gateway-DNS Lab

## 🎯 Objective
This lab demonstrates how to:
- Configure 4 VLANs on a Layer 2 switch.
- Assign IP addresses dynamically using DHCP from a router.
- Enable inter-VLAN communication using Router-on-a-Stick.
- Set default gateways and DNS settings for each VLAN.

---

## 🧱 Topology Overview
- 1 Router (with sub-interfaces for each VLAN)
- 1 Layer 2 Switch
- 12 PCs (3 per VLAN)
- Trunk link between router and switch
- DHCP pools configured on the router

---

## 📊 VLAN Details

| VLAN ID | Department | IP Range         |
|---------|------------|------------------|
| 10      | HR         | 192.168.10.0/24  |
| 20      | FINANCE    | 192.168.20.0/24  |
| 30      | IT         | 192.168.30.0/24  |
| 40      | SALES      | 192.168.40.0/24  |

---

## ⚙️ DHCP & Gateway Configuration
Each VLAN has:
- A DHCP pool on the router
- Default gateway (router sub-interface IP)
- DNS server IP (e.g., 8.8.8.8)

Example DHCP config:
```bash
ip dhcp pool HR
 network 192.168.10.0 255.255.255.0
 default-router 192.168.10.1
 dns-server 8.8.8.8
