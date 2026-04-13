# NAT & PAT

## NAT
NAT stands for Network Address Translation. it is used to translates private IP into public IP address for internet communication.

## Why NAT is used
- Saves Public IP
- Add Security (internal IP hidden)
- Enable internet Access

## Types of NAT

### Static NAT
    map one private ip to one public ip address

### Dynamic NAT
    map multiple private ip address to pool of public ip addresseds. it's assigned ip dynamically.

### PAT (most used)
    PAT allows multiple devices to share a single public ip using different port numbers.

#### Example
You open a website
Your IP → 192.168.1.10
Router changes → Public IP
Sends request to internet
Response comes back
Router maps back to your device

👉 NAT table handles mapping

## Port Forwarding
Allows external access to internal system via NAT.
Example:
Public IP:80 → Internal server:80
👉 Used for:
    Hosting website
    SSH access
