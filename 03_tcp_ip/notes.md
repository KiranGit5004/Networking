# TCP/IP Model

## Definition
TCP/IP is a 4-layer networking model used in real-world communication that defines how data is transmitted over the internet.

## Layers
1. Application – HTTP, DNS, FTP
2. Transport – TCP, UDP
3. Internet – IP, ICMP
4. Network Access – MAC, Ethernet

## Application Layer
it combines OSI layers: application, presentation, and session layer
handel user level protocols: http/https, ftp, dns, and smtp

## Transport Layer
it is similar to OSI Transport layer there are 2 main protocols 
TCP (reliable) and UDP (unreliable) 
it manages end to end data delivery, flow control, and error correction.

## Internet Layer
it is similar to OSI Network layer used logical addressing to routing data packet from source to destination networks
protocols: IP, ARP, ICMP.

## Network Access Layer
combines OSI layes 1 and 2 (data link and physical layer)
handel physical transmission of data, error detection, and MAC addressing.


## Explain TCP Three-Way handshake process?
The TCP Three-Way Handshake is a process used to establish a connection between a client and a server before data is transmitted. 
It involves three steps:
1. SYN (Synchronize): The client sends a SYN packet to the server to request a connection.
2. SYN-ACK (Synchronize-Acknowledge): The server responds with a SYN-ACK packet to acknowledge the client's request and signal readiness.
3. ACK (Acknowledge): The client sends an ACK packet back to the server, confirming the connection is established.

This handshake ensures both parties are synchronized and ready for data transmission.

## TCP (Transmission control protocol)
TCP is used when relibile delivery and order of data is important it provides connection-oriented communications.

## UDP (User datagram protocol)
UDP is used when speed is more imp than  reliability it offeres connectionless communications.
UDP is unreliable because it does not confirm whether the data is received or if it is received correctly. It simply sends data without establishing a connection or waiting for acknowledgments.
example: streaming, DNS lookups, gaming, etc... 

## OSI vs TCP/IP
OSI = 7 layers (theoretical)
TCP/IP = 4 layers (practical)   

## Questions
❓ Name all TCP/IP layers
✅ Answer:
Application, Transport, Internet, Network Access

❓ Difference between OSI and TCP/IP?
✅ Answer:
OSI has 7 layers and is theoretical, while TCP/IP has 4 layers and is used in real-world networking.

❓ What is TCP 3-way handshake?
✅ Answer:
It is a process to establish a connection:
SYN → SYN-ACK → ACK

❓ What is the role of Internet layer?
✅ Answer:
It handles IP addressing and routing between networks.

❓ TCP vs UDP?
✅ Answer:
TCP is reliable and connection-oriented, while UDP is faster and connectionless.

❓ What is a port?
✅ Answer:
A port is a logical endpoint used to identify specific services on a system.

❓ Which layer uses IP?
✅ Answer:
Internet Layer

❓ Which protocol is used for ping?
✅ Answer:
ICMP