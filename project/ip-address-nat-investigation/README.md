# IP Address & NAT Investigation (Hands-on Lab)

## Objective
The objective of this lab is to identify my device's private IP address, find my public IP address, compare both, and understand how Network Address Translation (NAT) works.

---

## Environment
- Device: MacBook
- OS: macOS
- Network: Wi-Fi (en0)

---

## Commands Used

### 1. Find Private IP Address
```bash
ifconfig
```
**Purpose:**
Displays network configuration details for all interfaces on the device.

**Result:**
Found under the `en0` interface (Wi-Fi):
```text
inet 172.20.10.2 netmask 0xffffff00 broadcast 172.20.10.255
```
Private IP Address: **172.20.10.2**

---

### 2. Attempted Linux Command (Not applicable on Mac)
```bash
ip a
```
**Result:**
Command not found (Mac does not support `ip` command)

---

## Screenshots

### Private IP Address
![Private IP](private-ip.png)

### Public IP Address
![Public IP](public-ip.png)

---

## Results

| Item | Value |
|------|-------|
| Private IP Address | 172.20.10.2 |
| Public IP Address | 102.88.113.33 |

---

## Analysis
The private IP address (172.20.10.2) is assigned to my device within the local network. It is not accessible from the internet.

The public IP address is assigned by the Internet Service Provider (ISP) and represents my network on the internet.

This shows that my device uses different addresses for local and internet communication.

---

## NAT Explanation
Network Address Translation (NAT) is a process used by routers to translate private IP addresses into a public IP address.

This allows multiple devices on the same
