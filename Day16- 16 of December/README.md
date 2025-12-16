# 🎄Advent of Cyber 2025 – Day 16🎄
### Forensics - Registry Furensics

---

## 🎯 Objective 

Understand what the Windows Registry is and how it can be used in digital forensics to investigate system and user activity by analyzing registry hive files in a safe, read-only way.

---

## 🛠 Tools & Techniques Used

- Windows Registry concepts (hives, keys, values)
- Registry Editor (for understanding structure)
- Registry Explorer (offline forensic analysis)
- Offline Registry Hive files:
    - SYSTEM
    - SOFTWARE
    - SAM
    - SECURITY
    - NTUSER.DAT
- Basic forensic investigation techniques

---

## 🧠 What I Learned Today

- The Windows Registry stores important system and user activity data
- Registry data is split into hives, each with a different purpose
- For forensic investigations, registry hives should be analyzed offline
- Registry Explorer allows safe analysis without modifying evidence
- The registry can reveal:
    - Computer name
    - User activity
    - Connected devices
    - Programs that were run or set to start automatically

---

## 📌 Step-by-Step Summary

**1.** Learned what the Windows Registry is and how it works

**2.** Identified the main Registry hives and what information they store

**3.** Mapped registry hive files on disk to registry keys shown in Registry Editor

**4.** Launched Registry Explorer for offline analysis

**5.** Loaded registry hive files from the provided evidence folder

**6.** Replayed transaction logs to ensure clean and complete hive data

**7.** Navigated registry keys to extract forensic information

**8.** Identified system details such as the computer name

**9.** Understood how registry data helps build an investigation timeline
  
---

## 🔐 Key Cybersecurity Concepts

- Windows Registry – A database storing system and user configuration
- Registry Hives – Separate files that store different categories of data
- Digital Forensics – Investigating systems after an incident
- Offline Analysis – Analyzing evidence without modifying it
- Evidence Integrity – Ensuring data remains unchanged during analysis

---

## 🖼️ Screenshots

![registry explorer](screenshots/01-.png)
*Registry Explorer launched and ready for offline registry forensic analysis.* ⬆️

![offline windows registry](screenshots/02-.png)
*Folder containing offline Windows registry hive files and associated transaction logs used for forensic analysis.* ⬆️

![System registry](screenshots/03-.png)
*Registry Explorer showing the SYSTEM registry hive being selected and loaded for offline forensic analysis.* ⬆️

![uninstall key](screenshots/04-.png)
⬆️ *This screenshot shows the Windows Registry Uninstall key, which stores information about applications installed on the system. By examining install dates and publisher details, it is possible to identify software that was added around the time abnormal activity began.*

**After loading the registry hives, I explored different registry locations to answer the questions in this task. Since there was no step-by-step guidance, I had to decide where to look based on the registry cheat sheet provided at the start of the room.
I checked registry keys that show installed applications to see what software had been added around the time the abnormal activity started. I then looked at user-related registry data to understand how applications were launched and from where.
Finally, I reviewed common startup and persistence registry locations to see if any application was set to run automatically when the system starts**


![day 16 completed](screenshots/Day16-completed.png)
*Proof of completing Day 16.* ⬆️

---

## ✅ Final Takeaway

This task helped me understand that the Windows Registry keeps a lot of information about how a system and its users behave. By using Registry Explorer to analyze registry files offline, I could safely look for evidence without changing anything. This showed me how forensic analysts use the registry to understand what happened on a system after an incident.
