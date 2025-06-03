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
- Select your **active network interface** (usually `Ethernet` or `Wi-Fi`) from the list.
- Click the blue **shark fin icon** or press `Ctrl + E` to start capturing.

---

## 🌐 3. Generate Network Traffic

- While capturing is active, open a web browser and:
  - Visit any website (e.g., `https://example.com`)
  - Or open a terminal/command prompt and run:  
    ```bash
    ping google.com
    ```

---

## ⏱️ 4. Stop the Capture After a Minute

- Let the capture run for about 1 minute to collect enough traffic.
- Click the red **stop icon** or press `Ctrl + E` again to stop capturing.

---

## 🔎 5. Filter Captured Packets by Protocol

Use the **display filter bar** at the top to filter traffic by protocol. Examples:

- HTTP:
