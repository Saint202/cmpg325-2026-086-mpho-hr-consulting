# CMPG325-2026-086 — Mpho HR Consulting Network Design

**Student:** Morake, TM (39510484)
**Client:** Mpho HR Consulting (Klerksdorp) — Professional Services
**Technical Challenge:** VLANs (switch-based segmentation design) — Intermediate
**Course:** CMPG 325 — Computer Networks, North-West University

## Project Summary

This repository documents the design, implementation, and testing of a segmented
office network for Mpho HR Consulting, built and simulated in Cisco Packet Tracer.
The network uses VLAN-based segmentation across four departments (Finance, HR,
General Staff, Guest/WiFi), with Finance fully isolated from all other departments
per the client's design constraint, and is provisioned to absorb 8 additional staff
in General Staff (Client Change Request CR1) without any redesign.

## Repository Structure

```
/requirements       Client requirements and Milestone 1 design review document
/design              Physical & logical topology diagrams, IP addressing plan
/packet-tracer       The .pkt file and any exported device configurations
/testing             Connectivity test screenshots and verification evidence
/troubleshooting     Notes on issues encountered during the build and their fixes
```

## Key Design Facts

| Item | Detail |
|---|---|
| Address block | 172.30.58.0/23 |
| VLAN 10 | Finance — 172.30.58.0/26 (isolated via ACL) |
| VLAN 20 | HR — 172.30.58.64/26 |
| VLAN 30 | General Staff — 172.30.58.128/26 (CR1 growth) |
| VLAN 40 | Guest/WiFi — 172.30.58.192/26 |
| Routing | Router-on-a-stick (single Gi0/0, dot1Q subinterfaces) |
| Isolation | Extended ACL `ISOLATE_FINANCE` applied on all subinterfaces |
| Addressing | DHCP, one pool per VLAN |

## Project Milestones

- [x] Milestone 1 — Client Design Review (28 Aug 2026)
- [ ] Milestone 2 (2 Oct 2026)
- [ ] Final Submission (16 Oct 2026)

## Academic Integrity

This project was completed individually per NWU CMPG 325 requirements. AI assistance
(where used) does not transfer responsibility for the submitted work — all design
decisions, configuration, and verification are my own understanding and work.
