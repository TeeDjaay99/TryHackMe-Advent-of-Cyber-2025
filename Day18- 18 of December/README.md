# 🎄Advent of Cyber 2025 – Day 18🎄
### Obfuscation - The Egg Shell File

---

## 🎯 Objective 

The objective of Day 18 was to understand and reverse different obfuscation techniques used to hide malicious content.
By analyzing encoded and layered data, I practiced identifying patterns and using CyberChef to safely decode hidden information without executing it.

---

## 🛠 Tools & Techniques Used

- CyberChef
- Base64 encoding / decoding
- ROT ciphers (ROT1, ROT13, ROT47)
- XOR obfuscation
- Gzip compression
- Pattern recognition
- PowerShell script review (static analysis)

---

## 🧠 What I Learned Today

- Obfuscation is often used to hide intent, not to make malware “advanced”
- Many obfuscation techniques leave visual patterns that can be recognized
- Layered obfuscation must be reversed in the correct order
- CyberChef makes complex decoding much easier when used step by step
- You should always analyze suspicious scripts without executing them

---

## 📌 Step-by-Step Summary

**1.** Reviewed the explanation of common obfuscation techniques

**2.** Identified patterns in encoded strings

**3.** Used CyberChef to test decoding methods one step at a time

**4.** Reversed layered obfuscation in the correct order

**5.** Analyzed the PowerShell script statically to understand its behavior
  
---

## 🔐 Key Cybersecurity Concepts

- Obfuscation – Techniques used to hide readable data
- Layered obfuscation – Multiple encoding methods combined
- Static analysis – Inspecting code without running it
- Pattern recognition – Using visual clues to identify encoding types
- Safe malware analysis – Never executing unknown scripts direc

---

## 🖼️ Screenshots

![Own YARA Rule](screenshots/01-Running-containers.png)

![Own YARA Rule](screenshots/01-Running-containers.png)

![Own YARA Rule](screenshots/01-Running-containers.png)

![Own YARA Rule](screenshots/01-Running-containers.png)
*Proof of completing Day 18.* ⬆️

---

## 🧭 Investigation Approach

I started by reading the task explanation carefully to understand what kind of obfuscation might be used.
Instead of immediately decoding everything, I looked for patterns such as:
  - Strings that look like Base64
  - Text that is readable but “shifted” (ROT-style ciphers)
  - Output that looks random but keeps the same length (XOR)

Once I had a reasonable guess, I recreated the transformations in CyberChef.
For layered obfuscation, I applied the decoding steps in reverse order, removing one layer at a time until the content became readable.
When reviewing the PowerShell script, I focused on understanding what the code does, not running it. This helped me safely analyze potentially malicious logic without risking execution.

---

## ✅ Final Takeaway

Day 18 helped me understand that obfuscation is mainly about slowing down analysis, not preventing it.
By staying calm, recognizing patterns, and reversing transformations step by step, even heavily obfuscated data can be understood safely.
This felt very realistic and reinforced the importance of methodical analysis over rushing.
