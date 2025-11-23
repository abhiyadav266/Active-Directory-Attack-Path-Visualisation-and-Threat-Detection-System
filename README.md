![License](https://img.shields.io/badge/License-MIT-green.svg)

# 🛡 Active Directory Attack Path Visualisation & Threat Detection System

A hybrid cybersecurity lab that demonstrates **how attackers compromise an Active Directory domain** and **how defenders detect and investigate these attacks in real time using Sysmon + Wazuh SIEM**.

The project covers the **complete kill chain**:  
➡ **Red Team** — Attack, Exploitation & Lateral Movement  
➡ **Blue Team** — Detection, Alerting & Incident Response

---

## 📌 Project Objective
Simulate an end-to-end enterprise breach — from **initial AD enumeration to domain privilege escalation and lateral movement**, and detect every malicious activity using **Sysmon telemetry, Wazuh rules, Windows Event IDs, and MITRE ATT&CK mapping**.

---

## ⚠ Phase-A — Red Team Attack Simulation (Offensive)

| Step | Objective | Attack Technique | Tools Used |
|------|-----------|------------------|------------|
| 1 | Enumerate AD objects & sessions | Domain Recon | BloodHound / SharpHound |
| 2 | Identify privilege escalation path | Attack Graph Mapping | BloodHound |
| 3 | Extract Kerberos service tickets | Kerberoasting | Impacket-GetUserSPNs / Rubeus |
| 4 | Identify privilege misconfigurations | Local Enumeration | WinPEAS |
| 5 | Dump credentials from LSASS memory | Credential Theft | Mimikatz |
| 6 | Gain privileged access | Password & Login Brute Force | Hydra / RDP |
| 7 | Achieve full system shell | Remote Code Execution | Metasploit psexec |

📂 Screenshots + command logs stored in:  
`/Phase-A-RedTeam/`

---

## 🟢 Phase-B — Blue Team Threat Detection & Response (Defensive)

| Detection Category | Log Source | Status |
|--------------------|------------|--------|
| Process Execution Monitoring | Sysmon | ✔ |
| Kerberoasting Detection | Sysmon + Wazuh Rules | ✔ |
| Credential Dumping (Mimikatz) | Windows Security Logs | ✔ |
| Privilege Escalation Attempt | Wazuh Dashboard | ✔ |
| Unauthorized Admin Login | Event ID Monitoring | ✔ |
| Lateral Movement (SMB / RDP) | Telemetry + MITRE Mapping | ✔ |

📂 Screenshots + alert evidence stored in:  
`/Phase-B-BlueTeam/`

---

## 🧠 Key Cybersecurity Concepts Demonstrated
🔹 AD Attack Path Visualisation using BloodHound  
🔹 Kerberos Abuse — TGS extraction & hash cracking  
🔹 Privilege Escalation via misconfiguration analysis (WinPEAS)  
🔹 Credential dumping from memory using Mimikatz  
🔹 Pass-the-Hash & remote lateral movement (psexec)  
🔹 Sysmon endpoint telemetry and event correlation  
🔹 Wazuh SIEM for real-time threat analytics and alerting  
🔹 MITRE ATT&CK technique mapping for classification & response  

---

## 🏗 Lab Architecture (Enterprise Cyber Range)

| Component | Role |
|----------|------|
| Windows Server 2019 | Domain Controller |
| Windows 10 | Domain-Joined Client |
| Kali Linux | Red Team Attacker |
| Ubuntu Server | Wazuh SIEM |
| Sysmon | Endpoint Telemetry Provider |
| Wazuh Dashboard | Log Analytics & Alerting |

---

## 🧩 Tool Stack
`BloodHound · SharpHound · Hydra · WinPEAS · Mimikatz · Metasploit · Impacket · Rubeus · Sysmon · Wazuh · Ubuntu · Windows Server · PowerShell`

---

## 🔥 Skills Gained
✔ Active Directory exploitation & hardening  
✔ Red Team attack automation & lateral movement  
✔ SIEM-based threat detection & SOC monitoring  
✔ Windows event analysis & credential abuse forensics  
✔ Incident handling, alert triage & MITRE ATT&CK mapping  

---

## 👤 Author
**Abhishek Yadav**  
Cybersecurity | Active Directory | Threat Detection | Red / Blue Team

---
⭐ If you found this project helpful, consider giving it a star!
