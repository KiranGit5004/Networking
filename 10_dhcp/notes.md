# DHCP (Dynamic Host Configuration Protocol)

## Definition
DHCP is used to automatically assign IP addresses and other network configuration settings such as subnet masks, gateways, and DNS servers to client devices on a network. by using DHCP we can automating the process of IP assignment and preventing the configuration error also save times. 

## Ports
   Protocol	      Port
- DHCP Server	   67
- DHCP Client  	   68

## DORA Process
1. Discover:
    Client broadcasts:
    “Any DHCP server available?”
2. Offer:
    Server replies:
    “Here’s an IP for you”
3. Request:
    Client says:
    “I accept this IP”
4. Acknowledge:
    Server confirms:
    “IP assigned”

👉 This full process = IP assignment

## Concepts
### Lease time
- IP is given for a limited time (lease time)
- After expiry → renewal happens
👉 Example:
Lease = 24 hours

### IP pool
Range of IPs

## APIPA
If DHCP fails → system assigns:
169.254.x.x
👉 Meaning:
💥 No DHCP server reachable

## Commands
- check IP: 
    ip addr

- Renew IP: 
    dhclient

- Release IP:
    dhclient -r

- Check logs:
    journalctl -u NetworkManager