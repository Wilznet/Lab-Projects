# CCNA 200-301 Mega Lab – Full Rebuild from Scratch

**Topology credit:** Jeremy’s IT Lab (excellent free CCNA video series)  
**My contribution:** I rebuilt the entire 10-part mega lab 100% from scratch in Packet Tracer using only Jeremy’s topology and requirements document – no copy-paste of his configs. This was my final CCNA consolidation project.

## Why I did this
- To prove I can configure every single CCNA topic end-to-end without looking at solutions  
- To have one massive, real-world-style lab for my portfolio  
- To be able to explain any line of configuration in an interview

## Topics Covered (literally everything on the exam except GRE)
- Hostnames, secrets, local users, console security
- L2 & L3 EtherChannel (LACP + PAgP)
- VLANs, trunks, DTP, VTPv2 server/client
- Access port config for PCs, IP phones, LWAPs
- STP root placement, PortFast, BPDU Guard
- HSRP 
- OSPF Single-area 
- NAT (static, PAT, pool)
- IPv4 ACLs (standard + extended)
- DHCP server + relay
- SSH, NTP, Syslog, SNMPv2
- WPA2-PSK wireless + controller basics
- Full IPv4 + IPv6 addressing scheme

- ## Important Note on Management Access
I intentionally left console  login authentication disabled (no “login local” or AAA) during the build.  
Reason: In a lab with 12 devices, having to type username/password every single time I opened a new CLI window slowed me down dramatically. This is purely a lab convenience — in real production networks I always enforce strong local or AAA authentication.

Everything else (enable secret, user accounts, line timeouts, synchronous logging, etc.) is fully configured as required.

## Files Included
- `CCNA-Mega-Lab-Final.pkt` – fully working Packet Tracer file (saved with all configs)
- `topology-full.png` – complete topology screenshot
- `final-configs/` – clean running-config of every router & switch (named clearly)
- `requirements.pdf` – Jeremy’s original task list (for reference & transparency)

Everything works 100 % – VLANs propagate, OSPF neighbors are up, HSRP active/standby correct, NAT & ACLs tested, wireless clients associate, IPv6 works, etc.

Feel free to download, open the .pkt, and throw any verification command you want – it will pass.

Thanks Jeremy for the amazing free content that made this possible!  
