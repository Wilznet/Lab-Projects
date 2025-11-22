# Remote Access IPsec VPN Lab (CCNA-level)

100 % built and tested by me from scratch in Packet Tracer.

## Objective
Configure a classic remote-access IPsec VPN so a SOHO user (PC0) can securely connect to the Headquarters network and reach 192.168.2.0/24 resources.

## Topology
- SOHO Router (1941) — 192.168.1.0/24 LAN + public serial to ISP
- ISP Router (2901) — transit only
- HQ Router (1941) — VPN head-end with crypto map + dynamic map + local user + address pool

## Key Configurations Implemented
- IKEv1 Phase 1 policy (AES-256, SHA, DH Group 5)
- Transform-set (esp-aes esp-sha-hmac)
- Dynamic crypto map + crypto map applied to serial interface
- ISAKMP client group "groupvpn" with pre-shared key ciscokey
- Local IP pool 192.168.2.10–15
- AAA authentication/authorization for VPN clients
- Local username admin / password (encrypted)
- NAT overload on SOHO with proper ACL 
- Static default routes

## What Works
- PC0 (using built-in Windows VPN client) connects successfully
- Receives 192.168.2.x address from pool
- Can ping HQ LAN (192.168.2.1) and PC1 inside HQ
- show crypto isakmp sa → ACTIVE
- show crypto ipsec sa → packets encrypt/decrypt counters increasing

## Files
- `Remote-Access-IPsec-VPN.pkt` — open and everything works immediately
- `final-configs/` — clean running-configs of all three routers
- `verification-screenshot` — exact commands to prove the VPN is up

Lab completed 100 % manually — no copy-paste, no saved solutions.  

Feel free to clone and test.
