# 🛡️ ProtonVPN Free Setup

---

## 🧩 Step-by-Step Guide

### 🔹 Step 1: Choose a Free VPN

I use **ProtonVPN** — a privacy-respecting VPN with a free plan.

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
```

🔹 Step 4: Connect to a VPN Server
  
  1. Open ProtonVPN app
  2. Click Quick Connect or select a Free Server
  3. Wait until it says "Connected"

🔹 Step 5: Check Your IP Address

  1. Before and after connecting, visit https://whatismyipaddress.com:

🔸 Example (Before VPN):

```
IP: 105.22.113.78  
Location: Lagos, Nigeria  
ISP: MTN Nigeria
```

🔸 Example (After VPN Connected):
```
IP: 185.159.157.6  
Location: Amsterdam, Netherlands  
ISP: ProtonVPN AG

```

🔹 Step 6: Verify Traffic Is Encrypted
  1. Visit any HTTPS website (e.g., https://example.com)
  2. Look for the padlock icon 🔒 in the browser address bar
  3. Press F12 → go to Network tab
  4. Check that all requests are using HTTPS
  5. This means your traffic is encrypted and secure.

🔹 Step 7: Check Speed Before and After VPN
  Use https://www.speedtest.net to compare:

🔸 Without VPN:
```
Ping: 12 ms  
Download: 92 Mbps  
Upload: 18 Mbps
```
🔸 With VPN:
```
Ping: 48 ms  
Download: 34 Mbps  
Upload: 7 Mbps
```

⚠️ Expect a slowdown when connected due to encryption and routing — this is normal.

🔹 Step 8: Research on VPN Technology
  1. ProtonVPN (Free) includes:
  2. Protocols: OpenVPN, WireGuard
  3. Encryption: AES-256 (military grade)
  4. DNS Leak Protection: Enabled by default
  5. No Logging: Strong no-logs privacy policy
  6. Open-source Clients: Transparent and audited

Learn more: https://protonvpn.com/blog/is-protonvpn-safe/

🔹 Step 9: Summary of VPN Benefits & Limitations

✅ Benefits:

  1. Hides your real IP address
  2. Encrypts your online activity
  3. Secures public Wi-Fi usage
  4. Bypasses geo-blocks (limited in free tier)
  5. Prevents ISP tracking and surveillance

⚠️ Limitations:

  1. Slower speeds (especially on free tier)
  2. Free servers limited to a few locations
  3. Some websites block VPN IPs (e.g., Netflix)
  4. Requires trust in the VPN provider
