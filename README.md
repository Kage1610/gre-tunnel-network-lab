# gre-tunnel-network-lab
GRE Tunnel with OSPF over Overlay (Cisco Packet Tracer)
# GRE Tunnel Network Lab

## 📌 Overview
This project demonstrates a GRE tunnel between two routers (R0 and R3) over an underlying routed network.

The goal is to allow communication between two LANs while restricting traffic between R0 and R1 to GRE only.

## 🧠 Technologies Used
- GRE Tunnel
- OSPF (over the tunnel)
- Static Routing (underlay)
- ACL (traffic restriction)

## 🏗️ Topology
![Topology](image.png)

## 📂 Router Configurations

All router configurations are organized in the `configs/` directory for clarity and reproducibility.

## ⚙️ How It Works
- Underlay network (R0-R1-R2-R3) provides basic connectivity
- GRE tunnel creates a virtual link between R0 and R3
- OSPF runs only inside the tunnel
- ACL ensures only GRE traffic passes between R0 and R1

## ✅ Verification
- Tunnel status: `show ip interface brief`
- OSPF neighbors: `show ip ospf neighbor`
- Routing table: `show ip route`
- End-to-end connectivity: ping between PCs

## 💡 Improvements
- Add IPsec for encryption
- Use loopback as tunnel source
- Add redundancy (backup tunnel)
