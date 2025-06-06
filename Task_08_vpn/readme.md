# 🛡️ ProtonVPN Free Setup, Testing, and Summary (All-in-One)

This guide walks you through everything you need to know and do — from installing a free VPN (ProtonVPN), connecting to a secure server, checking your IP address, verifying traffic encryption, testing speeds, researching how VPNs work, and summarizing benefits and limitations — all in one single file.

---

## 🧩 Step-by-Step Guide

### 🔹 Step 1: Choose a Free VPN

We will use **ProtonVPN** — a privacy-respecting VPN with a free plan.

- Website: [https://protonvpn.com](https://protonvpn.com)
- Reasons to choose:
  - 100% free tier (no data cap)
  - Strong encryption (AES-256)
  - No logs policy
  - Servers in 3 countries (Free tier): 🇺🇸 US, 🇳🇱 Netherlands, 🇯🇵 Japan

---

### 🔹 Step 2: Sign Up

1. Go to: [https://protonvpn.com/signup](https://protonvpn.com/signup)
2. Choose the **Free Plan**
3. Verify your email
4. Set your username and password

---

### 🔹 Step 3: Download and Install

#### 💻 For Windows/macOS:

- Visit: [https://protonvpn.com/download](https://protonvpn.com/download)
- Download the app for your OS
- Install and log in with your Proton account

#### 🐧 For Linux:

```bash
sudo apt install -y protonvpn-cli
protonvpn init

🔹 Step 4: Connect to a VPN Server
Open ProtonVPN app

Click Quick Connect or select a Free Server

Wait until it says "Connected"

🔹 Step 5: Check Your IP Address
Before and after connecting, visit https://whatismyipaddress.com:

🔸 Example (Before VPN):

IP: 105.22.113.78  
Location: Lagos, Nigeria  
ISP: MTN Nigeria


🔸 Example (After VPN Connected):

IP: 185.159.157.6  
Location: Amsterdam, Netherlands  
ISP: ProtonVPN AG



🔹 Step 6: Verify Traffic Is Encrypted
Visit any HTTPS website (e.g., https://example.com)

Look for the padlock icon 🔒 in the browser address bar

Press F12 → go to Network tab

Check that all requests are using HTTPS

✅ This means your traffic is encrypted and secure.

🔹 Step 7: Check Speed Before and After VPN
Use https://www.speedtest.net to compare:

🔸 Without VPN:
makefile
Copy
Edit
Ping: 12 ms  
Download: 92 Mbps  
Upload: 18 Mbps
🔸 With VPN:
makefile
Copy
Edit
Ping: 48 ms  
Download: 34 Mbps  
Upload: 7 Mbps
⚠️ Expect a slowdown when connected due to encryption and routing — this is normal.

🔹 Step 8: Research on VPN Technology
ProtonVPN (Free) includes:

Protocols: OpenVPN, WireGuard

Encryption: AES-256 (military grade)

DNS Leak Protection: Enabled by default

No Logging: Strong no-logs privacy policy

Open-source Clients: Transparent and audited

Learn more: https://protonvpn.com/blog/is-protonvpn-safe/

🔹 Step 9: Summary of VPN Benefits & Limitations
✅ Benefits:
Hides your real IP address

Encrypts your online activity

Secures public Wi-Fi usage

Bypasses geo-blocks (limited in free tier)

Prevents ISP tracking and surveillance

⚠️ Limitations:
Slower speeds (especially on free tier)

Free servers limited to a few locations

Some websites block VPN IPs (e.g., Netflix)

Requires trust in the VPN provider