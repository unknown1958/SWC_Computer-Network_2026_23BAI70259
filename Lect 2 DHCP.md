# Dynamic Host Configuration Protocol (DHCP)

## Introduction

Dynamic Host Configuration Protocol (DHCP) is a network protocol that automatically assigns IP addresses and other network configuration information to devices connected to a network.

### Why DHCP is Needed

- Eliminates manual IP configuration.
- Reduces configuration errors.
- Prevents duplicate IP addresses.
- Improves scalability.
- Simplifies network management.

### Benefits of DHCP

- Automatic IP Assignment
- Reduced Administrative Effort
- Prevention of IP Conflicts
- Centralized Management
- Better Scalability
- Faster Device Configuration

---

# DHCP Architecture

DHCP follows a client-server architecture.

```text
DHCP Client
     ↕
DHCP Server
```

## Components of DHCP

### DHCP Server

The DHCP Server manages and assigns IP addresses and network settings.

#### Responsibilities

- Assign IP addresses
- Manage leases
- Assign subnet masks
- Assign gateways
- Assign DNS servers

### DHCP Client

A device that requests network configuration information.

**Examples:**

- Laptop
- Smartphone
- Desktop
- Printer
- Smart TV
- IoT Device

### DHCP Relay Agent

Forwards DHCP messages between clients and servers located on different networks.

### IP Address Pool

A collection of available IP addresses maintained by the DHCP server.

### Lease Database

Stores:

- Assigned IP addresses
- MAC addresses
- Lease duration
- Assignment history

---

# DHCP Lease

A Lease is a temporary assignment of an IP address.

### Benefits

- Efficient IP utilization
- Address recycling
- Better scalability

---

# DHCP Working Process (DORA)

DORA is the four-step process used to obtain an IP address.

## D – Discover

The client broadcasts a request to locate DHCP servers.

### Purpose

- Find available DHCP servers.

## O – Offer

The server offers an available IP address.

### Information Included

- IP Address
- Subnet Mask
- Gateway
- DNS Server
- Lease Duration

## R – Request

The client requests the offered IP address.

### Purpose

- Accept the offered configuration.

## A – Acknowledgement (ACK)

The server confirms the IP assignment.

### Information Included

- Assigned IP Address
- Subnet Mask
- Gateway
- DNS Server
- Lease Duration

---

## DORA Flow Diagram

```text
Client
  ↓
Discover
  ↑
Offer
  ↓
Request
  ↑
ACK
Server
```

---

# DHCP Communication Types

## Broadcast

Sent to all devices on the network.

### Example

- DHCP Discover

## Unicast

Sent directly to a specific device.

### Example

- Lease Renewal

---

# DHCP Port Numbers

| Device | Port |
|----------|----------|
| DHCP Server | UDP 67 |
| DHCP Client | UDP 68 |

---

# DHCP Lease Management

## Lease Lifecycle

```text
Lease Assigned
      ↓
Lease Active
      ↓
T1 Renewal
      ↓
T2 Rebinding
      ↓
Lease Expires
```

### T1 Timer

- Occurs at 50% of lease duration.
- Contacts original DHCP server.
- Used for renewal.

### T2 Timer

- Occurs at 87.5% of lease duration.
- Contacts any available DHCP server.
- Used for rebinding.

### Lease Expiration

If renewal fails:

- Lease expires.
- IP becomes invalid.
- DORA process restarts.

---

# DHCP Messages

| Message | Purpose |
|----------|----------|
| Discover | Locate DHCP Servers |
| Offer | Offer Configuration |
| Request | Request Address |
| ACK | Confirm Assignment |
| NAK | Reject Assignment |
| Decline | Reject Offered Address |
| Release | Return Address |
| Inform | Request Additional Information |

---

# DHCP Address Allocation Methods

## Dynamic Allocation

- Temporary IP assignment
- Most common method
- Suitable for large networks

## Automatic Allocation

- Permanent IP assignment
- Address retained indefinitely

## Manual Allocation (Reservation)

- Fixed IP assigned based on MAC Address
- Suitable for servers and printers

---

# DHCP Reservation

DHCP Reservation ensures a device always receives the same IP address.

### Devices Using Reservation

- Printers
- File Servers
- CCTV Cameras
- Routers
- Network Switches

---

# DHCP Scope

A Scope defines the range of IP addresses available for assignment.

### Components

- Start IP Address
- End IP Address
- Subnet Mask
- Gateway
- DNS Information
- Lease Duration

---

# Exclusion Range

Addresses that DHCP should never assign.

### Example

```text
Scope:
192.168.1.100 - 192.168.1.200

Excluded:
192.168.1.100 - 192.168.1.110
```

---

# DHCP Options

Additional information provided by DHCP:

- Subnet Mask
- Default Gateway
- DNS Server
- Domain Name
- NTP Server
- TFTP Server

---

# DHCP Security

## Common Threats

### DHCP Starvation Attack

An attacker exhausts all available IP addresses.

### Rogue DHCP Server

An unauthorized DHCP server provides incorrect configuration.

### Man-in-the-Middle (MITM)

Traffic is redirected through attacker-controlled systems.

---

# DHCP Snooping

A security feature that prevents unauthorized DHCP servers.

## Benefits

- Prevents Rogue DHCP Servers
- Improves Security
- Supports Advanced Protection

### DHCP Snooping Binding Table

Stores:

- MAC Address
- IP Address
- VLAN Information
- Interface Information
- Lease Time

---

# DHCP Security Best Practices

1. Enable DHCP Snooping
2. Restrict DHCP Server Access
3. Monitor DHCP Logs
4. Use Secure Switch Configurations
5. Audit DHCP Settings Regularly

---

# DHCP Troubleshooting

## Common Problems

- DHCP Server Unavailable
- Scope Exhaustion
- DHCP Relay Failure
- Incorrect Configuration
- Network Connectivity Issues

## APIPA

Automatic Private IP Addressing (APIPA) is assigned when DHCP fails.

### APIPA Range

```text
169.254.0.0/16
```

### Meaning

- DHCP communication failed.
- No valid DHCP lease obtained.

---

# DHCP vs Static IP

| Feature | DHCP | Static IP |
|----------|----------|----------|
| Configuration | Automatic | Manual |
| Scalability | High | Low |
| Administrative Effort | Low | High |
| Flexibility | High | Low |
| Address Stability | Variable | Fixed |

---

# DHCPv6

DHCPv6 provides DHCP functionality for IPv6 networks.

## Features

- IPv6 Address Assignment
- DNS Configuration
- Domain Information
- Network Parameters

### Stateful DHCPv6

- DHCP Server assigns IPv6 addresses.
- Lease information maintained.

### Stateless DHCPv6

- Devices generate their own IPv6 addresses.
- DHCP provides additional configuration only.

### Advantages

- Supports IPv6 Networks
- Improved Scalability
- Better Address Management
- Future-Proof Architecture

---

# Advantages of DHCP

- Automatic Configuration
- Reduced Administrative Work
- Efficient IP Utilization
- Centralized Management
- Improved Scalability
- Simplified Deployment

---

# Disadvantages of DHCP

- Dependence on DHCP Server
- Security Risks
- Additional Infrastructure Requirements
- Potential Service Disruption

---

# Conclusion

DHCP is a fundamental networking protocol that automates IP address assignment and network configuration. Through DORA, lease management, reservations, and DHCPv6 support, it enables efficient and scalable network administration while reducing manual effort and configuration errors.

# Abbreviations

| Abbreviation | Full Form |
|-------------|-----------|
| DHCP | Dynamic Host Configuration Protocol |
| DORA | Discover, Offer, Request, Acknowledgement |
| IP | Internet Protocol |
| DNS | Domain Name System |
| MAC | Media Access Control |
| UDP | User Datagram Protocol |
| ACK | Acknowledgement |
| NAK | Negative Acknowledgement |
| APIPA | Automatic Private IP Addressing |
| DHCPv6 | Dynamic Host Configuration Protocol Version 6 |
| IPv4 | Internet Protocol Version 4 |
| IPv6 | Internet Protocol Version 6 |
| NTP | Network Time Protocol |
| TFTP | Trivial File Transfer Protocol |
| VLAN | Virtual Local Area Network |
| MITM | Man-in-the-Middle |
| CCTV | Closed-Circuit Television |
| IoT | Internet of Things |
| T1 | Lease Renewal Timer (50%) |
| T2 | Lease Rebinding Timer (87.5%) |
