# **Networking Fundamentals & Hands-on Checks**

# **OSI and TCP/IP Model**

# **OSI Model -**
OSI is a conceptual model that defines network communication. It consists of 7 layers where each layer performs a specific function.

Application L7 - User interaction (e.g., browser).
Presentation L6 - Data encryption/decryption, format conversion.
Session L5 - Establish/manage/terminate sessions.
Transport L4 - Reliable delivery (TCP/UDP).
Netwrok L3 - IP addressing, routing.
Data Link L2 - Error‑free node‑to‑node delivery.
Physical L1 - Hardware, cables, signals.

# **TCP/IP Model -**
TCP/IP is practically used for providing communication between computers over the internet.

Application L4 - Combines OSI’s Application + Presentation + Session.
Transport L3 - Same as OSI Transport.
Internet L2 - Same as OSI Network.
Netwrok access L1 - Physical + Data Link combined.

# **Protocol Placement**
IP, ICMP, ARP - Internet Layer  
TCP, UDP - Transport Layer
HTTP, HTTPS, FTP, SMTP, DNS, DHCP, SSH - Application layer
Ethernet, Wi-Fi - Network Access layer              


# **HANDS ONN**
<br></br>
<img width="870" height="626" alt="image" src="https://github.com/user-attachments/assets/4dab821c-1c9a-4bf2-816c-910689c04ff3" />
-- HTTP (Application) over TCP (Transport) over IP (Internet) <br></br>

# **Hands-on Checklist (run these; add 1–2 line observations)**
- Identity : hostname -I
-Reachability: ping <target>
-Path: traceroute <target>
<br></br>
  <img width="1575" height="994" alt="image" src="https://github.com/user-attachments/assets/88613646-1a93-404e-8c65-a8e5ea1c3d14" />
<br></br>

-Ports: ss -tulpn or netstat -tulpn
-Name resolution: dig <domain> or nslookup <domain>
-HTTP check: curl -I <http/https-url>
<br></br>
 <img width="1898" height="824" alt="image" src="https://github.com/user-attachments/assets/eca5f0b8-a827-4c30-a261-63dd42164f91" />
<br></br>

-Connections snapshot: netstat -an | head
<br></br>
<img width="711" height="245" alt="image" src="https://github.com/user-attachments/assets/638636b8-7ca7-4f67-a997-e37f04a74ddc" />
<br></br>


# **Reflection**

-Check firewall (sudo ufw status,sudo iptables -L -n -v)

-Service helth check (systemctl status <service>)

-Connectivity test (curl -I http://<server-ip>:<port>,nc -zv <server-ip> <port>)

-HTTP 500 : It is application layer. Since you got response(500) it means internet and transport layers are fine. Check at Application layer.

-- -> systemctl status service, journalctl -u service, tail -f /var/log/service/error.log
