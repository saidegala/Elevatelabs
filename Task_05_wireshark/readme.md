# Wireshark Packet Capture Guide

This guide provides a step-by-step walkthrough to perform a basic network packet capture using **Wireshark**, identify network protocols, and export the capture as a `.pcap` file.
 |a||
---

## 📦 1. Install Wireshark

- Download and install Wireshark from the official website: [https://www.wireshark.org/download.html](https://www.wireshark.org/download.html)
- Follow the installation instructions for your operating system (Windows, macOS, Linux).

---

## 📡 2. Start Capturing on Your Active Network Interface

- Open Wireshark.
- Select your **active network interface** (`Wi-Fi`) from the list.
- Click the blue **shark fin icon** or press `Ctrl + E` to start capturing.

---
## 🔎 3. Filter Captured Packets by Protocol

Use the **display filter bar** at the top to filter traffic by protocol. Examples:

- HTTP:
![image](https://github.com/user-attachments/assets/40f20428-474d-4ebc-8fa3-ea75259d7af6)

- TCP:
![image](https://github.com/user-attachments/assets/64bc7a84-e7af-4f1d-ba9b-bbafa8e99d22)

- UDP:
![image](https://github.com/user-attachments/assets/ab9b75fa-d59e-46ca-b9a1-a2580b93cfa5)

- DNS :
![image](https://github.com/user-attachments/assets/d716e254-aa0c-49a6-a381-1626503a29f4)

## 4. 📊 Protocol Summary

During the packet capture session, we observed multiple essential network protocols:

- **HTTP (HyperText Transfer Protocol):** This protocol is used for transferring web content. The capture shows typical HTTP GET requests and 200 OK responses, indicating successful web page loads over unencrypted connections.
  
- **DNS (Domain Name System):** DNS translates domain names (like `example.com`) into IP addresses. The capture includes standard DNS queries and responses, showing both IPv4 (A) and IPv6 (AAAA) lookups.

- **TCP (Transmission Control Protocol):** TCP ensures reliable, ordered delivery of data. The capture contains TCP handshakes (SYN, SYN-ACK, ACK) and application data exchange, particularly related to TLS-encrypted sessions.

- **UDP (User Datagram Protocol):** UDP is a lightweight, connectionless protocol. The capture shows it used for DNS queries and LLMNR (Local Link Multicast Name Resolution), which operate without needing a handshake or session.

These captures highlight how different protocols operate at various layers of the network stack to support web browsing and service discovery.

