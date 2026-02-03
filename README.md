# Network Intrusion Detection Lab: Cowrie Honeypot 🛡️

## 📌 Project Overview
As part of my transition into **Cybersecurity (Red Teaming)**, I deployed a honeypot environment to understand the dynamics of network attacks from a defender's perspective. 

This project involved setting up a **Cowrie Honeypot** (a medium-interaction SSH honeypot) to trap, log, and analyze a simulated brute-force attack.

## 🛠️ Tools & Technologies
* **Victim Machine:** Kali Linux (hosting Cowrie)
* **Attacker Machine:** Kali Linux (simulating threat actor)
* **Network Analysis:** Wireshark, Nmap
* **Virtualization:** Oracle VirtualBox (NAT Network isolation)

## ⚔️ Attack Simulation
I acted as the "Red Team" adversary to test the honeypot's defenses:
1.  **Reconnaissance:** Ran `nmap -A -p 2222` to identify the open SSH port.
2.  **Brute Force:** Executed an SSH login attack using common weak credentials.
3.  **Exploitation:** Upon gaining access to the deceptive shell, I ran enumeration commands (`whoami`, `ls -la`) which were logged by the system.

## 📊 Key Findings (Evidence)
The project successfully demonstrated the value of deception technology in network defense.

### 1. Nmap Discovery
*The scanner identified the open port 2222, mistaking the honeypot for a legitimate OpenSSH server.*
*(See attached screenshot: `nmap_scan_results.png`)*

### 2. Traffic Analysis (Wireshark)
*Captured the full TCP handshake and the subsequent failed authentication attempts in the attached `.pcap` file.*

## 📂 Files Included
* 📄 **Incident_Report.pdf**: A formal industry-standard report detailing the attack timeline and mitigation strategies.
* 📡 **honeypot_capture.pcap**: The Wireshark packet capture of the attack traffic.
* 📸 **Screenshots**: Visual proof of the lab setup and execution.

## 🚀 Conclusion
This lab reinforced the importance of:
* Moving SSH from default ports (Security through Obscurity).
* Using key-based authentication instead of passwords.
* The utility of honeypots for gathering threat intelligence.

---
*Documented by Israel Oluwasegun Emmanuel*
