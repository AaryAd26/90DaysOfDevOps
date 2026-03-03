# Networking Concepts: DNS, IP, Subnets & Ports

---

## Task 1: DNS – How Domain Names Resolve to IP Addresses

### 1. What happens when you type `google.com` in a browser?

**Answer:**

1. The browser first checks its local DNS cache to see if the IP address is already stored.
2. If not found, the system sends a DNS query to resolve the domain name into an IP address.
3. After receiving the IP address, the browser establishes a secure HTTPS connection using TCP/IP.
4. The request travels through routers and reaches load balancers.
5. The web server processes the request, may communicate with backend services (applications/databases), and sends back the webpage.

---

### 2. DNS Record Types

- **A** – Maps a domain name to an IPv4 address.
- **AAAA** – Maps a domain name to an IPv6 address.
- **CNAME** – Creates an alias from one domain to another.
- **MX** – Specifies the mail server responsible for emails.
- **NS** – Defines the authoritative name servers of the domain.

---

### 3. `dig google.com`

<img width="651" height="429" alt="Screenshot 2026-03-03 200415" src="https://github.com/user-attachments/assets/d9dbfcbd-3545-4b2d-930f-7f9cdd306bf7" />

---

## Task 2: IP Addressing

### 1. What is an IPv4 address?

An IPv4 address is a 32-bit numerical identifier assigned to devices in a network.

It has two parts:

- **Network Portion** – Identifies the network.
- **Host Portion** – Identifies the specific device.

**Example:** `192.168.1.10`  
- Network: `192.168.1.0`  
- Host: `10`

---

### 2. Public vs Private IP Addresses

| Public IP | Private IP |
|------------|------------|
| Assigned by ISP | Used within internal networks |
| Globally unique | Not routable on the internet |
| Example: `103.176.157.29`, `8.8.8.8` | Example: `192.168.x.x`, `10.x.x.x`, `172.16.x.x` |

---

### 3. Private IP Ranges

- `10.0.0.0 – 10.255.255.255`
- `172.16.0.0 – 172.31.255.255`
- `192.168.0.0 – 192.168.255.255`

---

### 4. Output of `ip addr show`

<img width="872" height="314" alt="image" src="https://github.com/user-attachments/assets/2a6f2997-f88d-4d1a-8ca9-825904af1e0f" />

---

## Task 3: CIDR & Subnetting

### 1. What does `/24` mean?

`/24` means the first 24 bits are used for the network portion.

- Total IPs: 256  
- Usable Hosts: 254  
- Range: `192.168.1.0 – 192.168.1.255`

---

### 2. Usable Hosts

- `/24` → 254  
- `/16` → 65,534  
- `/28` → 14  

---

### 3. Why Subnet?

Subnetting helps:

- Improve performance (reduces broadcast traffic)
- Increase security (isolates network segments)
- Simplify management and troubleshooting

---

### 4. CIDR Table

| CIDR | Subnet Mask       | Total IPs | Usable Hosts |
|------|------------------|-----------|--------------|
| /24  | 255.255.255.0    | 256       | 254          |
| /16  | 255.255.0.0      | 65,536    | 65,534       |
| /28  | 255.255.255.240  | 16        | 14           |

---

## Task 4: Ports – Entry Points to Services

### 1. What is a Port?

A port is a logical communication endpoint.

- IP address → Identifies the device.
- Port number → Identifies the service running on that device.

Ports allow multiple services to operate on the same machine.

---

### 2. Common Ports

| Port | Service |
|------|---------|
| 22   | SSH |
| 80   | HTTP |
| 443  | HTTPS |
| 53   | DNS |
| 3306 | MySQL |
| 6379 | Redis |
| 27017| MongoDB |

---

### 3. Listening Ports (`ss -tulpn`)

- Port 22 → SSH
- Port 80 → Apache2

---

## Task 5: Putting It Together

### 1. `curl http://localhost:80`

- Protocol: HTTP
- `localhost` → `127.0.0.1`
- Port `80` → Local web server

---

### 2. App Cannot Connect to `10.0.1.50:3306`

Check the following:

```bash
ss -tulpn | grep 3306
systemctl status mysql
nc -zv 10.0.1.50 3306
journalctl -u mysql
