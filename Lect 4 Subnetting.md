# Subnetting Computer Networks

## Overview

This repository contains comprehensive notes on **Subnetting in Computer Networks**, covering fundamental concepts, mathematical calculations, CIDR notation, FLSM, VLSM, route summarization, and real-world applications.

## Topics Covered

### Introduction to Subnetting
- Need for subnetting
- Historical background
- Benefits of subnetting
- Real-world examples

### IPv4 Fundamentals
- IPv4 address structure
- Binary number system
- Decimal to binary conversion
- Network ID and Host ID

### Subnet Masks and CIDR
- Subnet masks
- CIDR notation
- Classful addressing
- Private IP address ranges

### Subnetting Mathematics
- Borrowing bits
- Number of subnets calculation
- Number of hosts calculation
- Network address
- Broadcast address
- First and last host addresses

### Block Size Method
- Calculating block size
- Generating subnet ranges
- Fast subnetting techniques

### CIDR-Based Subnetting
- /24 to /30 subnet calculations
- CIDR reference tables
- Exam shortcuts

### FLSM and VLSM
#### FLSM (Fixed Length Subnet Mask)
- Equal-sized subnets
- Simple subnet planning

#### VLSM (Variable Length Subnet Mask)
- Variable-sized subnets
- Efficient IP utilization
- Address optimization

### Route Summarization
- Supernetting
- CIDR aggregation
- Route optimization

### Enterprise Applications
- University networks
- Corporate networks
- Data centers
- Cloud infrastructure

### Troubleshooting
- Common subnetting mistakes
- Interview questions
- Quick reference tables

---

## Important Formulas

### Number of Subnets

```text
Number of Subnets = 2^n
```

Where:
- n = Number of borrowed bits

### Number of Usable Hosts

```text
Usable Hosts = 2^h - 2
```

Where:
- h = Number of host bits

---

## Quick CIDR Reference

| CIDR | Subnet Mask | Usable Hosts |
|------|-------------|-------------|
| /24 | 255.255.255.0 | 254 |
| /25 | 255.255.255.128 | 126 |
| /26 | 255.255.255.192 | 62 |
| /27 | 255.255.255.224 | 30 |
| /28 | 255.255.255.240 | 14 |
| /29 | 255.255.255.248 | 6 |
| /30 | 255.255.255.252 | 2 |

---

## Learning Outcomes

After studying these notes, you will be able to:

- Understand IPv4 addressing
- Perform subnetting calculations
- Determine network and broadcast addresses
- Design FLSM and VLSM networks
- Apply route summarization techniques
- Solve networking interview questions

---

## Applications

Subnetting is widely used in:

- Enterprise Networks
- Universities
- Data Centers
- Cloud Platforms
- Internet Service Providers (ISPs)
- Government Organizations

## Abbreviations

| Abbreviation | Full Form |
|-------------|-----------|
| IP | Internet Protocol |
| IPv4 | Internet Protocol Version 4 |
| CIDR | Classless Inter-Domain Routing |
| FLSM | Fixed Length Subnet Mask |
| VLSM | Variable Length Subnet Mask |
| ISP | Internet Service Provider |
| LAN | Local Area Network |
| WAN | Wide Area Network |
| MAN | Metropolitan Area Network |
| VPC | Virtual Private Cloud |
| HR | Human Resources |
| IT | Information Technology |
| DNS | Domain Name System |
| DHCP | Dynamic Host Configuration Protocol |
| TCP | Transmission Control Protocol |
| UDP | User Datagram Protocol |
| MAC | Media Access Control |
| OSI | Open Systems Interconnection |
| NAT | Network Address Translation |
| VPN | Virtual Private Network |
| ICMP | Internet Control Message Protocol |
| ARP | Address Resolution Protocol |
| ISP | Internet Service Provider |
| ISP Router | Internet Service Provider Router |
