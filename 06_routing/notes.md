# Routing & Default Gateway

## Routing
Routing is the process of forwarding packets between networks using routers.

## Router
- Router is layer-3 device 
- Connects networks

## Default Gateway
- Router IP used to access other networks

## Routing Table
Contains destination and next hop info

Example:
0.0.0.0/0 → default route

## Types of Routhing

### Static Routing
- Static Routing is also known as non- adaptive routing
- Routers doesn't change routing tables unless admin change or modify it manually.
- it does not use routing algorithms.
- it is more secured and suitablr for small networks.

### Dynamic Routing
- Dynamic routing is also known as adaptive routing.
- Routers are sutomatically updated based on network changes.
- it uses routing protocols and algorithms (OSPF,RIP,BGP).
- it is suitablr for larg and complex networks.

#### 📌 Real Linux Commands (YOU MUST KNOW)
👉 Check IP:
ip addr

👉 Check routes:
ip route

👉 Add route:
ip route add

👉 Check connectivity:
ping google.com


#### 📌 REAL-WORLD SCENARIO (THIS GETS YOU JOB)
❌ Problem:
“No internet on system”

✅ Debug approach:
Check IP → ip addr
Check gateway → ip route
Ping gateway → ping 192.168.1.1
Ping external → ping 8.8.8.8
Check DNS → nslookup google.com

👉 This is real system admin thinking