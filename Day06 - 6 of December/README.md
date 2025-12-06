# 🎄Advent of Cyber 2025 – Day 06🎄
### Malware Analysis - Egg-xecutable

---

## 🎯 Objective 

Learn how to perform basic malware analysis using static and dynamic techniques inside a safe sandbox environment.
The goal is to understand what a suspicious executable does, how it behaves on a Windows system, and how tools like PeStudio, Regshot, and ProcMon help identify malicious actions.

---

## 🛠 Tools & Techniques Used

- PeStudio – static analysis (hashes, strings, imports, resources)
- Regshot – registry comparison before & after execution
- Process Monitor (ProcMon) – monitor process activity in real time
- Windows Sandbox / VM – safe environment for malware testing

---

## 🧠 What I Learned Today

- Malware can be examined without running it (static analysis) or by running it safely (dynamic analysis).
- Checksums, strings, and imports tell a lot about how an executable works.
- Regshot is great for spotting persistence techniques like Run keys.
- ProcMon reveals everything a sample touches: files, registry, network.
- Malware behaves quietly, but tools make its actions obvious when you know where to look.

---

## 📌 Step-by-Step Summary

**1.** Opened the VM and located the HopHelper.exe sample.

**2.** Loaded an example file in PeStudio to learn how to check:

  - SHA256 hash
  - Suspicious strings
  - Imports (libraries and functions)
  - Resources
    
**3.** Repeated the same steps on HopHelper.exe to answer analysis questions.

**4.** Used Regshot to take a 1st snapshot of the registry.

**5.** Executed HopHelper.exe in the sandbox.

**6.** Took the 2nd snapshot, compared differences, and saw new registry keys added (possible persistence).

**7.** Opened Process Monitor, started capturing system activity.

**8.** Ran the malware again to watch what it touched.

**9.** Applied filters to only show actions related to the executable (Process Name filter).

**10.** Observed operations like file writes, registry edits, and possibly network activity.
  
---

## 🔐 Key Cybersecurity Concepts

- Static Analysis: learning about malware without executing it.
- Dynamic Analysis: running malware safely to monitor behavior.
- Checksums (SHA256): unique identifiers for malware samples.
- Persistence Mechanisms: malware modifying registry keys to stay active.
- Process Monitoring: tracking all system-level interaction in real time.

---

## 🖼️ Screenshots



---

## ✅ Final Takeaway

Today really showed how malware isn’t “magic”—it’s just a program doing things behind the scenes.
With the right tools, even a beginner can reveal exactly what it tries to change, where it hides, and how it behaves.
Dynamic and static analysis together make malware feel a lot less scary and a lot more understandable.
