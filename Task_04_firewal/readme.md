# 🔥 Task 4 – Firewall Configuration on Windows

Hey there!  
This is my documentation for Task 4 where I worked on Windows Firewall. The goal was to learn how to create, test, and remove custom firewall rules — all without breaking the system 😅. I’ve written down every step I followed in a way that made sense to me.

---

## 🛠️ Step-by-Step Instructions

### 1. Open Windows Firewall Settings

- Click the **Start Menu**
- Search for and open **Windows Defender Firewall**
- OR go through:  
  `Control Panel > System and Security > Windows Defender Firewall`
- Once open, click on **Advanced Settings** in the left pane

👉 This opens a tool called **Windows Defender Firewall with Advanced Security**, which lets you configure inbound and outbound rules.

---

### 2. List Current Firewall Rules

- In the **Advanced Settings** window:
  - Click **Inbound Rules** to see all the current rules for incoming traffic
  - Click **Outbound Rules** to view rules for outgoing traffic
- You'll see a list of apps, ports, and services that have specific firewall permissions

📝 Take note of any rules that might already involve port 23 (we'll be working with that in the next step).

---

### 3. Block Inbound Traffic on Port 23 (Telnet)

To block connections coming into your system on Telnet's default port (23):

1. In the **Inbound Rules** section, click **New Rule…** (right-hand panel)
2. Select **Port**, then click **Next**
3. Choose **TCP**
4. Specify the port:  
   `Specific local ports:` → enter `23`, then click **Next**
5. Select **Block the connection**, then click **Next**
6. Apply the rule to all profiles: **Domain**, **Private**, and **Public**, then click **Next**
7. Name your rule something clear like `Block Telnet Port 23`
8. Click **Finish**

You’ve now blocked incoming traffic on port 23.

---

### 4. Test the Block Rule

Let’s check if port 23 is really blocked:

#### Option A – Use Telnet (if installed)

1. Open **Command Prompt**
2. Run:
   ```cmd
   telnet 127.0.0.1 23
