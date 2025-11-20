# CCNA Lab: GRE Point-to-Point Tunnels – Hub-and-Spoke Topology

 
This lab builds three GRE point-to-point tunnels between a hub router (Hub/HQ) and three spoke routers (Branch1/Spoke-1, Branch2/Spoke-2), runs OSPF only over the tunnels, and provides full reachability between all branch LANs while keeping the underlay simple and stable.

## Topology Overview
- Underlay: Serial links (10.1.x.0/30)
- Overlay: GRE tunnels (172.16.x.0/30)
- LANs: 192.168.1.0/24 (Branch3), 192.168.2.0/24 (Branch4), 192.168.3.0/24 (Branch5)

## Objectives Achieved
- Configured clean IP addressing on serial (underlay) and Ethernet (LAN) interfaces
- Created three point-to-point GRE tunnels with correct source/destination IPs
- Ran OSPF only over the tunnel interfaces (prevents recursive routing loops)
- Advertised branch LAN subnets via OSPF → full connectivity between all three branches
- Verified tunnel status, OSPF neighborships, routing tables, and end-to-end pings

## What You Will Learn
- Proper GRE tunnel configuration (source, destination, keepalives)
- Why OSPF is run only on tunnel interfaces in hub-and-spoke GRE designs
- How to avoid recursive routing issues
- Real-world stepping stone toward DMVPN (mGRE + NHRP + IPsec)

## Files in This Repository
- `GRE-Hub-and-Spoke-Topology.pkt` → Complete working Packet Tracer file
- `topology.png` → Screenshot of the topology
- `final-configs/` → Complete running-configs for all routers (copy-paste ready)
- `initial-configs/` → Minimal/clean starting configs (optional starting point)
- `verification-commands.txt` → Exact show/ping commands to prove everything works

## Quick Start
1. Open `GRE-Hub-and-Spoke-Topology.pkt` in Cisco Packet Tracer
2. (Optional) Load the configs from `final-configs/` or build manually
3. Open CLI on any router and run the commands in `verification-commands.txt`
4. You should see all tunnels UP, OSPF neighbors FULL, and pings succeeding between all three LANs

Enjoy the lab and feel free to improve it!
