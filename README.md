# University Network (Cisco Packet Tracer)

A simple **university network** built in **Cisco Packet Tracer** as a school project.

The topology contains **5 routers**:
- **R1 (Main/Core router)** connected to the Internet and to all branches.
- **R2 (Admin branch)** uses **Static Routing**.
- **R3 (Library branch)** uses **RIP**.
- **R4 (Labs branch)** uses **OSPF**.
- **R5 (Faculty branch)** uses **DHCP** for its LAN clients.

## Topology

![Topology]([University Network Topology](https://github.com/Meedooh13/University-Network/blob/edc747c25a5fee31b308550f4104aa0b7496088a/University%20Network%20Topology))

## IP Addressing Table

The following table summarizes the addressing used for router interfaces and LANs.

| Device | Interface | IP Address | Subnet Mask | Default Gateway |
|---|---|---|---|---|
| R1 | Se0/0/0 | 10.0.1.1 | 255.255.255.252 | N/A |
| R1 | Se0/0/1 | 10.0.2.1 | 255.255.255.252 | N/A |
| R1 | Se0/1/0 | 10.0.3.1 | 255.255.255.252 | N/A |
| R1 | Se0/1/1 | 10.0.4.1 | 255.255.255.252 | N/A |
| R2 | Se0/1/0 | 10.0.1.2 | 255.255.255.252 | N/A |
| R2 | Gig0/1 | 192.168.1.1 | 255.255.255.0 | N/A |
| R3 | Se0/1/0 | 10.0.2.2 | 255.255.255.252 | N/A |
| R3 | Gig0/1 | 192.168.2.1 | 255.255.255.0 | N/A |
| R4 | Se0/1/0 | 10.0.3.2 | 255.255.255.252 | N/A |
| R4 | Gig0/1 | 192.168.3.1 | 255.255.255.0 | N/A |
| R5 | Se0/1/0 | 10.0.4.2 | 255.255.255.252 | N/A |
| R5 | Gig0/1 | 192.168.4.1 | 255.255.255.0 | N/A |
| PCs (All) | NIC | `.2 / .3` (e.g., 192.168.x.2) | 255.255.255.0 | `192.168.x.1` |

> The raw addressing table is also included as: `Device-Interface-IPAddress-SubnetMask-DefaultGatew.csv`

## Subnets (Quick View)

### Point-to-Point WAN Links (/30)
- **R1–R2:** 10.0.1.0/30
- **R1–R3:** 10.0.2.0/30
- **R1–R4:** 10.0.3.0/30
- **R1–R5:** 10.0.4.0/30

### LAN Networks (/24)
- **Admin (R2):** 192.168.1.0/24
- **Library (R3):** 192.168.2.0/24
- **Labs (R4):** 192.168.3.0/24
- **Faculty (R5):** 192.168.4.0/24

## How to Use

1. Install **Cisco Packet Tracer**.
2. Open the Packet Tracer project file (typically `*.pkt`).
3. Verify routing between all LANs (ping between PCs across different branches).

## Notes

- This project is intended for learning and demonstration purposes.
- Each branch uses a different routing approach to practice multiple routing methods in the same topology.
