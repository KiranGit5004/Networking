# OSI Model

## Definition
OSI (Open Systems Interconnection) model is a 7-layer framework used to understand how data is transmitted over a network.

## Layers

### 7. Application
it is a interface between user and network providers  (HTTP/S, FTP, DNS)

### 6. Presentation 
it prepare data for application layer or session layer and Handles encryption and decryption, compression, formatting or Conversion

### 5. Session
it establish connection, manages, and terminate sessions between two devices

### 4. Transport
it provides reliable and unreliable data transmission through segmentation each segment consist sr.no, source and destination port addresses and data. 
example: 1) video call = UDP
         2) file download = TCP

### 3. Network
it Handles ip addresses and routing of data packets from source to destination across multiple networks.
Protocols: ip, ICMP, ARP
Devices: Router. 

### 2. Data Link
Uses MAC address, creates frames, and error detection data link layer transmit data node to node
Devices: Switch.

### 1. Physical
Transmits bits over cable or wireless in form of 0 and 1 

## Data Flow
Encapsulation:
Data → Segment → Packet → Frame → Bits

Decapsulation:
Reverse process at receiver

## Key Concepts
- Encapsulation
- Decapsulation

## Devices
- Hub → Layer 1
- Switch → Layer 2
- Router → Layer 3

### Questions
❓ Explain OSI model with real example

Answer:
The OSI model explains how data travels through 7 layers. For example, when accessing a website, the request starts at the Application layer, gets encrypted at Presentation, managed at Session, transferred via TCP at Transport, routed using IP at Network, framed with MAC at Data Link, and transmitted as bits at Physical layer.

❓ What is difference between Layer 2 and Layer 3?

Answer: Layer 2 (Data Link) uses MAC addresses for communication within a local network, while Layer 3 (Network) uses IP addresses for communication between different networks.

❓ Why do we need OSI model?

Answer: To standardize communication and simplify troubleshooting by dividing networking into layers.

❓ What happens if Transport layer fails?

Answer: Data delivery becomes unreliable—packets may be lost, duplicated, or out of order.

❓ Which layer does ping work on?

Answer: Network Layer (uses ICMP)

❓ Which layer does ARP work on?

Answer: Between Layer 2 and Layer 3 (Data Link + Network)
