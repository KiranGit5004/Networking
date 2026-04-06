# Subnetting

## What is Subnetting?
Subnetting is the process of dividing a large network into smaller sub-networks.

## Why Subnetting?
- Reduces network congestion
- Improves performance
- Enhances security
- Efficient IP address usage

## Key Terms
- Network ID → first IP
- Broadcast ID → last IP
- Usable IP → between them

## IP Address Structure
An IP address has two parts:
- Network Portion
- Host Portion

Example:
192.168.1.10/24

- /24 → Network bits
- Remaining bits → Host
---

## Formula
Total IPs = 2^(host bits)
Usable = Total - 2

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