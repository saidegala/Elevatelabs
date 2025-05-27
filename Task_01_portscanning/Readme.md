# 🔍 Task 1: Scan Local Network for Open Ports

To analyze network traffic in a local network, several tools can be used. For this task, the primary tools used were:

- **Wireshark** – Packet capture and analysis  
- **Nmap** – Network scanning and host discovery  
- Other useful tools: `tcpdump`, `netstat`

---

## 🛠️ Nmap Scan Overview

1. **Download & Install** Nmap from the official site: [nmap.org/download](https://nmap.org/download)  
2. **Scan Command Used**:
   ```bash
   nmap -sS -p- 192.168.1.0/24
   
 * Performs a stealth scan (-sS) on all ports (-p-) across the subnet.

 * Scan results can be saved (default format is .xml).

3. we can save the scan or download the scan default it is in xml extentison.

4. below you can see the example 

---

| IP Address     | Device Info          | Ports Identified                             |
|----------------|----------------------|----------------------------------------------|
| 192.168.1.138  | Unknown              | 5060/tcp (filtered – SIP)                   |
| 192.168.1.254  | Arcadyan Router      | 22 (filtered), 53 (open), 80 (open), 443 (open) |
| 192.168.1.130  | Likely Windows Host  | Multiple open/filtered ports (details below) |

---

These are my finding using Nmap , i found 3 devices connected to my network .

## 🔎 Detailed Findings

### 🖥️ 192.168.1.138 — Unknown Device

| **Open Port** | **Protocol/Use**     | **Commonly Found In**   | **Risk Level** | **Mitigation**                                               |
| -------- | -------------------- | ----------------------- | -------------- | ------------------------------------------------------------ |
| 5060     | SIP (VoIP signaling) | VoIP systems, IP phones | High           | Use firewalls, disable if unused, encrypt SIP (use TLS/5061) |

---

### 🌐 192.168.1.254 — Arcadyan Router (Default Gateway)

| **Open Ports** | **Protocol/Use**           | **Commonly Found In**      | **Risk Level** | **Mitigation**                                |
| -------- | -------------------------- | -------------------------- | -------------- | --------------------------------------------- |
| 53/tcp   | DNS (Domain Name System)   | DNS servers, network tools | Medium         | Restrict access, monitor traffic, use DNSSEC  |
| 80/tcp   | HTTP (Web traffic)         | Web servers, browsers      | High           | Use HTTPS instead, apply web server hardening |
| 443/tcp  | HTTPS (Secure web traffic) | Secure websites, APIs      | Medium         | Keep SSL/TLS updated, use strong ciphers      |

---

### 💻 192.168.1.130 — Likely Windows Host

| **Port** | **Protocol/Use**           | **Commonly Found In**              | **Risk Level** | **Mitigation**                                               |
| -------- | -------------------------- | ---------------------------------- | -------------- | ------------------------------------------------------------ |
| 135/tcp  | Microsoft RPC              | Windows systems (DCOM services)    | High           | Block externally, restrict access via firewall               |
| 139/tcp  | NetBIOS                    | Windows file/printer sharing       | High           | Disable if not needed, use SMB over TCP (445) instead        |
| 445/tcp  | SMB (Server Message Block) | Windows file sharing, AD services  | High           | Disable if unused, patch SMB vulnerabilities, firewall rules |
| 902/tcp  | VMware Service             | VMware ESXi, vSphere               | Medium         | Restrict to management network, update VMware software       |
| 912/tcp  | Apex Mesh                  | Possibly IoT or mesh systems       | Medium         | Investigate use, close if unnecessary                        |
| 5357/tcp | WSDAPI (Web Services)      | Windows devices (device discovery) | Medium         | Disable WSD if unused, limit network scope                   |
| 8090/tcp | Custom App or Messaging    | Web servers, chat apps             | Varies         | Confirm app usage, enforce authentication, monitor traffic   |


---

## 🛠️ Tools Used

- **Nmap** – Network scanning and host discovery  
  Scan Command:
  ```bash
  nmap -sS -p- 192.168.1.0/24
