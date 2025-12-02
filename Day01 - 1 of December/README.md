# Advent of Cyber – Day 01
**Topic: Linux CLI**

---

## 🎯 Objective 

Today's challenge introduced the Linux command-line interface and how to investigate a compromised system using basic CLI tools. The goal was to navigate the file system, read hidden files, analyze logs, inspect a suspicious shell script, switch users, and review bash history for traces left by attackers.

---

## 🛠 Tools & Techniques Used

- `echo` – Print text
- `ls`, `ls -la` – List files (including hidden)
- `cat` – Read file contents
- `cd` – Navigate directories
- `grep` – Search logs for specific patterns
- `find` – Locate files by name
- `sudo su` – Switch to root
- `history` – Review command history
- General Linux CLI usage

---

## 🧠 What I Learned Today

- How to navigate and explore Linux directories from the terminal  
- How hidden files (starting with `.`) can store important or suspicious information  
- Using `grep` to filter log output efficiently  
- Using `find` to locate potentially malicious scripts  
- How shell scripts work and how to interpret their commands  
- Why attackers often hide their tools in user directories  
- How to switch to the root user and why root access is powerful  
- How bash history can reveal attacker activity

---

## 📌 Step-by-Step Summary

---

## 🔐 Key Cybersecurity Concepts

- **Hidden Files** – Used by admins (and attackers) to store information out of plain view  
- **Log Analysis** – Reviewing `/var/log/auth.log` helps detect brute-force attempts  
- **Shell Scripts** – Commonly used for automation but also for malicious activity  
- **Privilege Escalation** – Accessing `root` provides full system control  
- **Forensics via Bash History** – Attackers often leave command traces after intrusion 

---

## 🖼️ Screenshots

---

## ✅ Final Takeaway

**Day 1 reinforced the importance of CLI proficiency, log analysis, hidden files, and basic forensics — all essential skills for SOC analysts and security investigators.**
