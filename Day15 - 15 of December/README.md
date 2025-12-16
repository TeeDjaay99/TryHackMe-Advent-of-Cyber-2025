# 🎄Advent of Cyber 2025 – Day 15🎄
### Web Attack Forensics - Drone Alone

---

## 🎯 Objective 

Investigate a suspected web-based attack by analyzing Apache and Windows logs in Splunk, with the goal of identifying command injection, process execution, and post-exploitation activity.

---

## 🛠 Tools & Techniques Used

- Splunk Enterprise (Search & Reporting)
- Apache access logs
- Apache error logs
- Sysmon (Windows process monitoring)
- Base64 decoding (external tool)
- Log correlation across multiple data sources

---

## 🧠 What I Learned Today

- How malicious web requests appear in Apache access logs
- How attackers hide commands using Base64-encoded PowerShell
- How to determine if a web attack reached the operating system
- How SOC analysts confirm exploitation using process creation logs

---

## 📌 Step-by-Step Summary

**1.** Logged into Splunk and verified access to the Search dashboard
**2.** Searched Apache access logs for suspicious keywords like cmd.exe and powershell

**3.** Identified Base64-encoded PowerShell commands inside HTTP requests

**4.** Decoded the payload to understand attacker intent

**5.** Checked Apache error logs for 500 Internal Server Errors

**6.** Used Sysmon logs to confirm Apache spawned cmd.exe

**7.** Detected attacker enumeration activity using the whoami command

**8.** Verified that no encoded PowerShell payload successfully executed
  
---

## 🔐 Key Cybersecurity Concepts

- Command Injection – executing system commands through a vulnerable web app
- SIEM (Splunk) – centralized log analysis for detection and investigation
- Base64 Encoding – obfuscation technique used by attackers
- Process Correlation – linking web activity to OS-level execution
- Post-Exploitation Reconnaissance – attacker actions after gaining execution

---

## 🖼️ Screenshots

![Own YARA Rule](screenshots/01-Running-containers.png)

![Own YARA Rule](screenshots/01-Running-containers.png)

![Own YARA Rule](screenshots/01-Running-containers.png)

![Own YARA Rule](screenshots/01-Running-containers.png)

![Own YARA Rule](screenshots/01-Running-containers.png)

![Own YARA Rule](screenshots/01-Running-containers.png)

![Own YARA Rule](screenshots/01-Running-containers.png)

![Own YARA Rule](screenshots/01-Running-containers.png)


---

## ✅ Final Takeaway

