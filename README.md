# Windows Firewall – Block & Allow Port Example

## 📌 Objective
Configure Windows Firewall to block inbound traffic on a specific port (Port 23 – Telnet), test the block, and then remove the rule to restore normal traffic flow.

---

## 🛠 Tools Used
- **Windows Defender Firewall** (with Advanced Security)
- **Telnet Client** (enabled via Windows Features)
- **Command Prompt**

---

## 🔹 Steps Performed

### 1️⃣ View Current Rules
- Opened **Windows Defender Firewall with Advanced Security**.
- Checked existing **Inbound Rules**.
- **Screenshot:**  
  ![Inbound Rules](firewall_inbound_rules.png)

---

### 2️⃣ Create Block Rule for Port 23
- In **Inbound Rules**, selected **New Rule → Port → TCP → 23 → Block the connection**.
- Applied to all profiles (Domain, Private, Public).
- Named it **Block Telnet Port 23**.
- **Screenshot:**  
  ![Create Rule Port 23](firewall_create_rule_port23.png)

---

### 3️⃣ Test the Block
- In Command Prompt, ran:
  ```cmd
  telnet localhost 23
  
- Output:
- Connecting To localhost...
-Could not open connection to the host, on port 23: Connect failed



-**📚** What I Learned

 -   Inbound Rules control incoming traffic; Outbound Rules control outgoing.

 -    Firewalls can block/allow based on port, protocol, or application.

 -    Even if the firewall allows a port, the connection fails if no service is listening.

 -  Blocking unused or risky ports (like Telnet) improves security.


