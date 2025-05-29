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
- Provide your name and email (used [tempmail](https://temp-mail.org/en/) for business email)
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
| 🔴 Critical   | 0   |
| 🟠 Medium     | 02     |
| 🟢 Low        | 0    |
|  info         | 0 | 


---
## 🔍 Critical Vulnerabilities & Mitigations

### 🔴 1. SMB Signing Not Required
- **Risk**: Without SMB signing, attackers on the same network can perform man-in-the-middle (MITM) attacks, intercepting or altering SMB traffic.
- **Fix**:
  - Enable SMB signing via Group Policy:
    - `Computer Configuration > Windows Settings > Security Settings > Local Policies > Security Options`
    - Set **Microsoft network client: Digitally sign communications (always)** to **Enabled**
  - Reboot to apply changes

### 🔴 2. SSL Certificate Cannot Be Trusted
- **Risk**: The server is using an SSL certificate that is self-signed or not issued by a trusted certificate authority, which could allow attackers to impersonate the server.
- **Fix**:
  - Replace the certificate with one signed by a trusted Certificate Authority (CA)
  - Ensure the full certificate chain is installed
  - Use tools like [SSL Labs Test](https://www.ssllabs.com/ssltest/) to verify
---

## 📂 Notes

- Nessus Essentials allows scanning up to **16 IPs**
- Full scans may consume significant resources and time
- Always update Nessus plugins before starting scans

---

