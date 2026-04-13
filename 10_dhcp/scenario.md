# 🚀 DHCP Troubleshooting Scenarios (Interview + Real World)

---

##  SCENARIO 1 — APIPA ISSUE

###  Problem:
User system shows:
```
169.254.23.10
```
No internet.

###  What most people say:

👉 “Network issue”
❌ Wrong. Too vague.

###  Correct Thinking:
👉 Step-by-step:

```bash
ip addr
```

* Confirms APIPA
* Means → DHCP failed

###  Check:

* Is cable connected?
* WiFi connected?
* DHCP server running?

###  Root Cause:

DHCP server not reachable OR network issue

###  Interview Answer:

“169.254.x.x indicates DHCP failure. I would check connectivity, DHCP server status, and try renewing IP using dhclient.”

---

##  SCENARIO 2 — SOME SYSTEMS GET IP, OTHERS DON’T

###  Problem:

* 10 systems working
* 5 systems not getting IP

###  Your Approach:

* Check working system IP range
* Check DHCP pool

###  Root Cause:

👉 IP pool exhausted

###  Example:

```
Range: 192.168.1.1 – 192.168.1.10
Devices: 15
```

###  Interview Answer:

“I would check DHCP pool size. If exhausted, I’ll extend the range or reduce lease time.”

---

##  SCENARIO 3 — IP ASSIGNED BUT NO INTERNET

###  Problem:

* IP: 192.168.1.20 ✅
* Internet ❌

###  Don’t jump to DHCP!

👉 DHCP already worked (IP assigned)

###  Check:

#### Gateway:

```bash
ip route
```

#### DNS:

```bash
nslookup google.com
```

###  Root Cause:

* Wrong gateway
* Wrong DNS

###  Interview Answer:

“Since IP is assigned, DHCP is working. I would check gateway and DNS configuration.”

---

##  SCENARIO 4 — IP CONFLICT

###  Problem:

User gets message:
👉 “IP address conflict detected”

###  What’s happening?

Two devices using same IP

###  Steps:

#### Check IP:

```bash
ip addr
```

#### Ping same IP:

```bash
ping 192.168.1.x
```

###  Root Cause:

Static IP overlapping DHCP pool

###  Interview Answer:

“I would check for duplicate IP usage and ensure DHCP range does not overlap with static IPs.”

---

##  SCENARIO 5 — IP CHANGES FREQUENTLY

###  Problem:

User IP keeps changing every hour

###  Think:

👉 DHCP lease issue

###  Root Cause:

Very short lease time

###  Fix:

Increase lease time on DHCP server

###  Interview Answer:

“Frequent IP change indicates short DHCP lease time. I would increase lease duration.”

---

##  SCENARIO 6 — DHCP SERVER DOWN

###  Problem:

Entire office:

* No IP assigned
* All systems → APIPA

###  Thinking:

👉 This is not client issue
👉 This is central failure

###  Root Cause:

DHCP server down

###  Action:

* Restart DHCP service
* Check logs

###  Interview Answer:

“If all systems fail to get IP, I would check DHCP server availability and service status.”

---

##  SCENARIO 7 — DIFFERENT NETWORK DHCP ISSUE

###  Problem:

DHCP server in another network
Clients not getting IP

###  Think:

👉 DHCP uses broadcast
👉 Broadcast doesn’t cross routers

###  Root Cause:

No DHCP relay

###  Fix:

Configure DHCP relay

###  Interview Answer:

“I would configure DHCP relay because DHCP broadcast cannot cross networks.”

---

##  SCENARIO 8 — WRONG IP RANGE ASSIGNED

###  Problem:

System gets:

```
10.0.0.x
```

But network should be:

```
192.168.1.x
```

###  Think:

👉 Wrong DHCP server

###  Root Cause:

Rogue DHCP server

###  Interview Answer:

“This indicates a rogue DHCP server. I would identify and remove it.”

---

#  Key Takeaway

Stop giving generic answers like:
❌ “Network issue”

Start thinking like:
✅ Identify layer
✅ Identify service
✅ Identify root cause

That’s what separates average candidates from hires.