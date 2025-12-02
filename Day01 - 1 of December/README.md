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

1. Displayed a message using `echo`  
2. Listed directory contents with `ls`  
3. Navigated to the `Guides` directory with `cd`  
4. Used `ls -la` to reveal hidden files  
5. Opened the hidden guide using `cat .guide.txt`  
6. Followed the guide to `/var/log` to investigate logs  
7. Used `grep "Failed password"` to identify failed login attempts  
8. Used `find /home/socmas -name "*egg*"` to locate a suspicious script  
9. Analyzed the `eggstrike.sh` script to understand its behavior  
10. Switched to root with `sudo su` and checked bash history  
11. Identified attacker commands left behind in `.bash_history`

---

## 🔐 Key Cybersecurity Concepts

- **Hidden Files** – Used by admins (and attackers) to store information out of plain view  
- **Log Analysis** – Reviewing `/var/log/auth.log` helps detect brute-force attempts  
- **Shell Scripts** – Commonly used for automation but also for malicious activity  
- **Privilege Escalation** – Accessing `root` provides full system control  
- **Forensics via Bash History** – Attackers often leave command traces after intrusion 

---

## 🖼️ Screenshots

![Listing hidden files]()
*Using `ls -la` to reveal hidden guide file.*

---

## ✅ Final Takeaway

**Day 1 reinforced the importance of CLI proficiency, log analysis, hidden files, and basic forensics — all essential skills for SOC analysts and security investigators.**
