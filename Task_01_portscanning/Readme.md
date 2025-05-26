# 🔐 Internal Network Scan Report

This repository contains results and analysis from an internal network scan performed using **Nmap**. The scan identifies open/filtered ports, assesses potential security risks, and provides remediation steps for each identified device.

---

## 📋 Summary

| IP Address     | Device Info          | Ports Identified                             |
|----------------|----------------------|----------------------------------------------|
| 192.168.1.138  | Unknown              | 5060/tcp (filtered – SIP)                   |
| 192.168.1.254  | Arcadyan Router      | 22 (filtered), 53 (open), 80 (open), 443 (open) |
| 192.168.1.130  | Likely Windows Host  | Multiple open/filtered ports (details below) |

---

## 🔎 Detailed Findings

### 🖥️ 192.168.1.138 — Unknown Device

- **Filtered Port:**
  - `5060/tcp` – SIP (Session Initiation Protocol)

- **Risk:**
  - May indicate a VoIP device. SIP is often targeted for eavesdropping or unauthorized access.

- **Mitigation:**
  - Disable SIP service if not required.
  - Ensure VoIP system uses secure transport (TLS/SRTP).
  - Restrict access to known IPs or internal subnets.

---

### 🌐 192.168.1.254 — Arcadyan Router (Default Gateway)

- **Open Ports:**
  - `53/tcp` – DNS
  - `80/tcp` – HTTP
  - `443/tcp` – HTTPS

- **Filtered Port:**
  - `22/tcp` – SSH

- **Risk:**
  - Web interface may be exposed.
  - Open DNS may be exploited for tunneling.
  - SSH visibility increases brute-force attack risk.

- **Mitigation:**
  - Disable HTTP; enforce HTTPS with strong credentials.
  - Restrict management access by IP.
  - Disable remote SSH or use key-based authentication.
  - Update router firmware regularly.

---

### 💻 192.168.1.130 — Likely Windows Host

- **Open Ports:**
  - `135/tcp` – Microsoft RPC
  - `139/tcp` – NetBIOS
  - `445/tcp` – SMB
  - `902/tcp` – VMware Service
  - `912/tcp` – Apex Mesh
  - `5357/tcp` – WSDAPI
  - `8090/tcp` – Possibly messaging or custom app

- **Filtered Ports (examples):**
  - `25/tcp` – SMTP  
  - `143/tcp` – IMAP  
  - `587/tcp` – Submission  
  - `1433/tcp` – MS SQL  
  - ...many others

- **Risk:**
  - Legacy services (NetBIOS/SMB) are frequent attack vectors.
  - Third-party software may be outdated or misconfigured.
  - Numerous filtered ports indicate service visibility to attackers.

- **Mitigation:**
  - Disable unused legacy protocols (NetBIOS, SMBv1).
  - Patch Windows host and third-party services.
  - Restrict access via local firewall or ACLs.
  - Use endpoint protection and monitoring.

---

## ✅ Recommendations

- 🔐 **Segmentation** – Separate routers, VoIP, and user devices via VLANs.
- 🔒 **Least Privilege** – Restrict unnecessary port access across the network.
- 📊 **Monitoring** – Enable logging for all key services and use IDS/IPS.
- 🔄 **Patch Management** – Regularly update firmware and operating systems.
- 🛠️ **Repeat Scans** – Perform monthly Nmap scans to detect changes.

---

## 🛠️ Tools Used

- **Nmap** – Network scanning and host discovery  
  Scan Command:
  ```bash
  nmap -sS -p- 192.168.1.0/24
