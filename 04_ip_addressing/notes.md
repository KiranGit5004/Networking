# IP Addressing

## Definition
IP address is a unique logical identifier assigned to devices in a network.

## IPv4 
- 32-bit address
- divided into 4 octets (0–255)
- each octet is separated by dots (".")
  eg:- 123.89.46.72 

## IPv6 
- 128-bits address
- create to deal with the shortage of IPv4 addresses
- it is consists of 8 group of four hexadecimal digits separated by colon (":")
  eg:- 2001:0DC8:E004:0001:0000:0000:F00A 

## Network vs Host
- Network ID → identifies network
- Host ID → identifies device

## Types
### Private IP
it's used within local network / private network (like home or office)
private IP are not accessible from the internet

### Public IP
- Used to identify devices on the internet
- assigned by ISP and accessible globally

## Static vs Dynamic
- Static → fixed
- Dynamic → DHCP assigned

## Classes
- Class A → 1–126
- Class B → 128–191
- Class C → 192–223

## Special IP
- 127.0.0.1 → Loopback
- Broadcast → last IP
- Network → first IP

## What is Subnetting?
Subnetting is the process of dividing a large network into smaller sub-networks.

## Why Subnetting?
- Reduces network congestion
- Improves performance
- Enhances security
- Efficient IP address usage


## IP Address Structure
An IP address has two parts:
- Network Portion
- Host Portion

Example:
192.168.1.10/24

- /24 → Network bits
- Remaining bits → Host

---

## Subnet Mask

| CIDR | Subnet Mask |
|------|-------------|
| /24  | 255.255.255.0 |
| /25  | 255.255.255.128 |
| /26  | 255.255.255.192 |
| /27  | 255.255.255.224 |
| /28  | 255.255.255.240 |


## Example 1: 192.168.1.0/24 divided into 2 subnets

### Step 1: Borrow 1 bit
New CIDR = /25

### Step 2: Calculate Hosts
2^(32-25) - 2 = 126 hosts

---

### Subnet 1:
Network: 192.168.1.0  
Range: 192.168.1.1 – 192.168.1.126  
Broadcast: 192.168.1.127  

---

### Subnet 2:
Network: 192.168.1.128  
Range: 192.168.1.129 – 192.168.1.254  
Broadcast: 192.168.1.255  