🔐 Linux Network Security Lab

This repository demonstrates Linux-based network security by configuring firewall rules with UFW to protect the gateway and secure the network within a virtual machine environment. The lab covers network discovery, mapping, and firewall hardening.

1️⃣ Network Identification & Connectivity Verification

Objective: Confirm network interfaces, IP addresses, and connectivity.

Steps:

Use ip addr to list network interfaces and IPv4/IPv6 addresses.

Verify network connectivity with ping to the gateway or external host.

Outcome: Confirmed active interfaces and verified connectivity to the network.

✅ This step ensures the host is properly integrated within the network before performing any security operations.

![network](labredes.png)

2️⃣ Gateway Discovery & Network Mapping

Objective: Identify the default gateway and map the internal network topology.

Commands & Steps:

Identify the default gateway:

ip route

This provides the IP address of the gateway (critical for access control).

Use Nmap to perform active host discovery and network mapping:

Outcome: Mapped active hosts, open ports, and network layout, providing a foundation for firewall configuration.

⚡ Technical Note: Nmap scanning helps identify vulnerable hosts and services, crucial for defining precise firewall rules.

![network](labredes2.png)

3️⃣ Firewall Configuration with UFW (Uncomplicated Firewall)

Objective: Harden the host and gateway against unauthorized access.

Step 1 — Default Deny Incoming Traffic

sudo ufw default deny incoming

Blocks all inbound connections by default.

Reduces attack surface by denying unsolicited traffic.

Step 2 — Allow Secure Remote Access (SSH)

sudo ufw allow ssh

SSH is used for encrypted remote administration.

Only authorized remote access is permitted.

Step 3 — Enable UFW

sudo ufw enable

Activates all configured firewall rules.

Step 4 — Verify Active Rules

sudo ufw status verbose

Displays open ports, allowed services, and default policies.

Outcome: Network traffic is tightly controlled; only permitted connections can reach the system.

🛡 Gateway protection is critical, as it represents a primary target for cyber intrusions.

✅ Security Impact

Default deny policy blocks unsolicited inbound traffic.

SSH access is explicitly allowed, reducing unauthorized login attempts.

Active monitoring ensures the gateway remains protected.

Establishes a hardened baseline for network security within Linux environments.

📚 Skills Demonstrated

Network interface and connectivity verification (ip addr, ping)

Gateway discovery (ip route)

Network mapping and host discovery (Nmap scanning)

Firewall hardening with UFW

Linux security administration and monitoring

📌 Conclusion

This lab provides a hands-on practical demonstration of Linux network security principles. It reinforces the importance of gateway protection, precise access control, and monitoring, forming the foundation for advanced cybersecurity practices.


![network](labredes3.png)
