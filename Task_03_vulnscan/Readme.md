# 🛡️ Basic Vulnerability Scan Using Nessus Essentials

## 📌 Task Overview
This task involves performing a basic vulnerability scan on a local Windows machine using **Nessus Essentials**. The goal is to identify security flaws and document critical vulnerabilities along with possible mitigations.

---

## ✅ Task Checklist

1. ✅ Install Nessus Essentials  
2. ✅ Set scan target to local machine IP (`localhost` or `127.0.0.1`)  
3. ✅ Start a full vulnerability scan  
4. ✅ Wait for scan to complete  
5. ✅ Review and analyze scan report  
6. ✅ Research basic mitigations for critical issues  
7. ✅ Document the most critical vulnerabilities  
8. ✅ Capture screenshots of results  

---

## 🛠️ Setup & Installation

### 📥 Download & Install Nessus Essentials
- Visit: [https://www.tenable.com/products/nessus/nessus-essentials](https://www.tenable.com/products/nessus/nessus-essentials)
- Provide your name and email (used [tempmail](https://tempmail.lol) for business email)
- Download and install Nessus for your OS
- Enter the activation code sent to your email
- Set up username and password
- Wait for **plugin compilation** (may take 30–60 mins)

---

## 🌐 Access Nessus Interface

- Open browser and go to:  
  `https://localhost:8834`

---

## 🎯 Create & Launch Scan

1. Click **New Scan**
2. Choose **Basic Network Scan**
3. Set:
   - **Name**: `My PC Scan`
   - **Target**: 
     - Run `ipconfig` in Command Prompt to get your local IP  
     - Or use `localhost` / `127.0.0.1`
4. Click **Save** → Click **Launch**

---

## 📝 Scan Results

| Severity     | Count |
|--------------|-------|
| 🔴 Critical   | X     |
| 🟠 Medium     | Y     |
| 🟢 Low        | Z     |

> *(Replace X, Y, Z with actual numbers from your report)*

---

## 🔍 Example Critical Vulnerabilities & Mitigations

### 🔴 1. Outdated Software Detected (e.g., OpenSSL)
- **Risk**: Allows remote code execution or man-in-the-middle attacks
- **Fix**: Update to the latest version from the official vendor

### 🔴 2. SMBv1 Enabled
- **Risk**: Vulnerable to EternalBlue (used in WannaCry)
- **Fix**: Disable SMBv1 via Windows Features or Group Policy

### 🔴 3. Remote Desktop Exposed Without Network Level Authentication
- **Risk**: Brute-force attack surface
- **Fix**: Enable NLA, use strong passwords, or disable RDP

> You can find detailed CVE references and suggested patches inside Nessus report results.

---

## 📂 Notes

- Nessus Essentials allows scanning up to **16 IPs**
- Full scans may consume significant resources and time
- Always update Nessus plugins before starting scans

---

