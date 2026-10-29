# CCNA
STP, PortFast,MST
# CCNA Switching Labs: STP, PortFast & MST

## Overview

This repository documents my hands-on networking labs as part of my CCNA 200-301 studies.

The project focuses on Layer 2 switching technologies, including Spanning Tree Protocol (STP), PortFast, BPDU Guard, and Multiple Spanning Tree (MST).

Using a redundant switching topology, I will explore how switches prevent Layer 2 loops, elect root bridges, handle redundant links, and improve network convergence.

## Network Topology

![STP, PortFast, and MST Lab Topology](topology/STP.png)

The lab topology consists of:

- **2 distribution switches:** DSW1 and DSW2
- **4 access switches:** SW1, SW2, SW3, and SW4
- **2 routers:** R1 and R2
- **Redundant Layer 2 links** between the switches
- **4 VLANs** for different departments

## VLAN and IP Addressing Plan

| VLAN | Name | Network |
|---|---|---|
| 10 | Operations | 192.168.10.0/24 |
| 20 | Logistics | 192.168.20.0/24 |
| 30 | Medical | 192.168.30.0/24 |
| 40 | Comms | 192.168.40.0/24 |

## Lab Objectives

### 1. Spanning Tree Protocol (STP)

- Understand how STP prevents Layer 2 switching loops.
- Identify the root bridge and root ports.
- Understand designated ports and alternate/blocking ports.
- Examine STP path costs and port roles.
- Verify spanning-tree operation using Cisco IOS commands.
- Observe how STP responds when links fail or recover.

### 2. PortFast and BPDU Guard

- Configure PortFast on appropriate end-device access ports.
- Understand why PortFast should not be enabled indiscriminately on switch-to-switch links.
- Configure BPDU Guard to protect edge ports.
- Test the behavior of a port when it receives a BPDU.
- Verify port status and recover from an err-disabled condition when appropriate.

### 3. Multiple Spanning Tree (MST)

- Understand MST regions, revision numbers, and VLAN-to-instance mappings.
- Configure MST on compatible switches.
- Map VLANs 10, 20, 30, and 40 to MST instances.
- Verify MST root bridges, port roles, and forwarding states.
- Explore load balancing by selecting appropriate roots for different instances.

## Verification Commands

```text
show spanning-tree
show spanning-tree vlan 10
show spanning-tree summary
show spanning-tree mst
show spanning-tree mst configuration
show interfaces status
show running-config
```

Command availability and syntax may vary by switch platform and software version.

## Repository Structure

```text
CCNA/
├── README.md
├── topology/
│   └── STP.png
├── labs/
│   ├── STP/
│   ├── PortFast-BPDU-Guard/
│   └── MST/
└── configs/
```

## Learning Approach

Each lab will include the objective, topology, configuration steps, verification commands, observed results, and troubleshooting notes.

My goal is to build practical networking skills, strengthen my understanding of switching technologies, and document my progress toward the CCNA certification.

**Status:** In progress 🚧
