# 📁 15_linux_networking_labs

Hands-on Linux networking labs using Virtual Machine environments like Oracle VM VirtualBox, VMware Workstation, or KVM.

Use RHEL, Ubuntu, Rocky Linux, AlmaLinux, or any Linux distro.

---

# 📄 01_check_ip.md

## Objective

Check current IP address, interface details, and network status.

## Commands

```bash id="lab1"
ip addr
hostname -I
nmcli device status
```

## Expected Result

* IP address visible
* Interface name (eth0 / ens33 / enp0s3)
* Connection state connected/disconnected

---

# 📄 02_static_ip_config.md

## Objective

Configure static IP in Linux.

## Command (RHEL / Rocky / AlmaLinux)

```bash id="lab2"
nmcli con mod ens33 ipv4.addresses 192.168.1.50/24
nmcli con mod ens33 ipv4.gateway 192.168.1.1
nmcli con mod ens33 ipv4.method manual
nmcli con up ens33
```

## Verify

```bash id="lab3"
ip addr
ip route
```

---

# 📄 03_ping_test.md

## Objective

Test connectivity between systems and internet.

## Commands

```bash id="lab4"
ping 192.168.1.1
ping 8.8.8.8
ping google.com
```

## Learning

* Gateway test
* Internet IP test
* DNS test

---

# 📄 04_dns_testing.md

## Objective

Test DNS resolution.

## Commands

```bash id="lab5"
nslookup google.com
dig google.com
cat /etc/resolv.conf
```

## Learning

* Domain to IP conversion
* DNS server config

---

# 📄 05_ssh_between_vms.md

## Objective

Connect one Linux VM to another using SSH.

## Setup

```bash id="lab6"
VM1: 192.168.1.10
VM2: 192.168.1.20
```

## On Target VM

```bash id="lab7"
systemctl enable --now sshd
```

## Connect

```bash id="lab8"
ssh user@192.168.1.20
```

---

# 📄 06_firewall_rules.md

## Objective

Allow and block ports.

## Commands

```bash id="lab9"
firewall-cmd --list-all
firewall-cmd --add-service=ssh --permanent
firewall-cmd --add-port=80/tcp --permanent
firewall-cmd --reload
```

---

# 📄 07_gateway_issue_lab.md

## Objective

Simulate wrong gateway issue.

## Command

```bash id="lab10"
ip route del default
```

## Result

* Local network may work
* Internet fails

## Restore

```bash id="lab11"
ip route add default via 192.168.1.1
```

---

# 📄 08_no_internet_troubleshooting.md

## Objective

Follow troubleshooting flow.

## Commands

```bash id="lab12"
ip addr
ip route
ping 192.168.1.1
ping 8.8.8.8
nslookup google.com
```

## Flow

IP → Gateway → Internet → DNS

---

# 📄 09_nat_vm_lab.md

## Objective

Understand NAT in VM networking.

## VirtualBox Example

* NAT Mode → Internet works
* Internal Network → VM to VM only
* Bridged Adapter → Gets LAN IP

## Learning

Understand NAT, private IP, internet access.

---

# 📄 10_port_checking.md

## Objective

Check listening ports and services.

## Commands

```bash id="lab13"
ss -tuln
netstat -tuln
```

---

# 📄 11_trace_route.md

## Objective

Trace packet path.

## Command

```bash id="lab14"
traceroute google.com
```

---

# 📄 12_dhcp_renew.md

## Objective

Renew DHCP IP.

## Commands

```bash id="lab15"
dhclient -r
dhclient
ip addr
```

---

# 🎯 Final Goal

After completing these labs you should be able to:

* Configure IP
* Diagnose connectivity issues
* Test DNS
* Use SSH
* Manage firewall
* Understand NAT
* Troubleshoot real network problems
