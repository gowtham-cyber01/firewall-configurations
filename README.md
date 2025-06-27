# firewall-configurations

## 📝 Task Title:
**Setup and Use a Firewall on Linux**

---

## 🎯 Objective:
Configure and test basic firewall rules using **UFW (Uncomplicated Firewall)** on a Linux system to allow or block specific network traffic.

---

## 📋 Task Instructions:

1. Open firewall configuration tool (UFW on Linux).
2. List current firewall rules.
3. Add a rule to block inbound traffic on a specific port (e.g., 23 for Telnet).
4. Test the rule by attempting to connect to that port locally or remotely.
5. Add rule to allow SSH (port 22).
6. Remove the test block rule to restore original state.
7. Document commands or GUI steps used.
---

## 🧰 Tools Used:
- **Kali Linux**
- **UFW (Uncomplicated Firewall)**
- **Telnet** (for testing blocked ports)
- **Linux Terminal**

---

## 🛠️ Step-by-Step Implementation:

### ✅ 1. Open the Firewall Tool:
Opened Linux Terminal and used UFW (installed via apt).

- **sudo apt update**
- **sudo apt install ufw**

### ✅ 2. List Current Firewall Rules
- **sudo ufw status**
- This shows the current firewall rules and whether UFW is active.
sudo ufw status numbered
-Lists the rules with numbers for easy removal.

### ✅ 3. Add Rule to Block Port 23 (Telnet)
- **sudo ufw deny 23**
- This blocks inbound traffic on port 23 to protect against insecure Telnet connections.

### ✅ 4. Test the Rule
- **telnet localhost 23**
-result: Connection refused (proves the firewall rule is active and working).

### ✅ 5. Add Rule to Allow SSH (Port 22)
- **sudo ufw allow 22**
-This ensures that SSH connections are still allowed for remote access.

### ✅ 6. Remove the Test Block Rule
- **sudo ufw delete 22**
