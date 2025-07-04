
---

## 🔍 Task 2: Analyze a Phishing Email Sample.

### 1. Check Email Headers for Discrepancies
- Tools: [MXToolbox](https://mxtoolbox.com/EmailHeaders.aspx), [Google Header Analyzer](https://toolbox.googleapps.com/apps/messageheader/)
- Look for:
  - `Return-Path` mismatch
  - Failed SPF/DKIM/DMARC
  - Suspicious IP in `Received` fields

📸 <img src="screenshots/email_headers_analysis.jpg" alt="Email Headers Analysis" width="1080" height="500" />

---

### 2. Examine the Sender's Email Address
- Watch for spoofed or misspelled domains 

📸 <img src="screenshots/spoofed_email_address.png" alt="Spoofed Email Address" width="1080" height="400" />


---

### 3. Identify Suspicious Links
- Hover over links without clicking
- Ensure URLs match their claimed domain 

📸 <img src="screenshots/mismatched_url_hover.jpg" alt="Mismatched URL Hover" width="1080" height="500" />

---

### 4. Look for Urgent or Threatening Language
- Common phrases include:
  - "Your account has been suspended"
  - "You must act now"
  - "Final warning!"

📸 <img src="screenshots/threatening_language.png" alt="Threatening Language" width="1080" height="500" />

---

### 5. Check for Spelling or Grammar Errors
- Phishing emails often contain awkward phrasing, misspellings, or odd formatting

📸 <img src="screenshots/grammar_errors.png" alt="Grammar Errors" width="1080" height="500" />

---

## ✅ Summary of Phishing Traits Found

| Trait                        | Status | Notes                                 |
|-----------------------------|--------|---------------------------------------|
| Spoofed sender address      | ✅     | Mismatched domain in From field       |
| SPF/DKIM/DMARC failed       | ✅     | Header authentication failed          |
| Mismatched or fake URLs     | ✅     | Hover revealed phishing destination   |
| Urgent/threatening tone     | ✅     | Message pressures immediate action    |
| Spelling/grammar issues     | ✅     | Multiple typos and formatting errors  |

---

## 📚 Screenshot References

Screenshots used in this report are from trusted educational resources:

- [Norton – Phishing Email Examples](https://us.norton.com/blog/online-scams/phishing-email-examples)
- [CanIPhish – 40 Phishing Email Templates](https://caniphish.com/phishing-email-examples)
- [HubSpot – Phishing Scenarios](https://blog.hubspot.com/marketing/phishing-email-examples)
- [Firewall Times – Common Phishing Types](https://firewalltimes.com/phishing-email-examples/)
- [The SSL Store – Best & Worst Examples](https://www.thesslstore.com/blog/phishing-email-examples-the-best-worst/)

---

## 🧰 Tools Used

- [Google Messageheader Tool](https://toolbox.googleapps.com/apps/messageheader/)
- [MXToolbox Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx)
- [VirusTotal](https://www.virustotal.com/)
- [Have I Been Pwned](https://haveibeenpwned.com/)

---

