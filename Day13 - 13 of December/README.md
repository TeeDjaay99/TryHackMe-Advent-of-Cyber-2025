# 🎄Advent of Cyber 2025 – Day 13🎄
### YARA Rules - YARA mean one!

---

## 🎯 Objective 

The goal of today’s lab was to understand what YARA is, why defenders use it, and how to write basic YARA rules to detect malicious files based on patterns instead of file names or hashes.

---

## 🛠 Tools & Techniques Used

- YARA
- Pattern matching (strings, hex, regex)
- Malware detection logic
- Basic rule writing and testing
- Command-line scanning with yara

---

## 🧠 What I Learned Today

Today I learned that YARA isn’t about finding a specific known malware file, but about spotting patterns that malware leaves behind.
Instead of relying only on antivirus signatures, YARA lets defenders describe what suspicious files might look like using things like text strings, byte patterns, and simple rules.
This helped me understand how analysts can search for suspicious behaviour, even when they don’t know exactly what the malware is yet.

---

## 📌 Step-by-Step Summary

**1.** Learned what YARA is and where it’s used in blue team workflows

**2.** Explored the structure of a YARA rule:
  - meta
  - strings
  - condition

**3.** Learned different string types:
  - Text strings
  - Wide / ASCII strings
  - XOR and Base64 strings
  - Hexadecimal patterns
  - Regular expressions

**4.** Practiced writing simple YARA rules

**5.** Ran YARA rules against files to detect malicious matches

**6.** Completed the practical task by scanning files and extracting the correct result

---

## 🔐 Key Cybersecurity Concepts

**YARA Rules**

YARA rules allow defenders to describe malware using identifiable patterns rather than relying on filenames or hashes.

**Strings & Patterns**

Malware often reuses strings, URLs, commands, or byte sequences that can be matched reliably.

**Conditions**

Conditions control when a rule triggers and help reduce false positives.

**Detection vs Prevention**

YARA is mainly a detection and hunting tool, often used after an incident or during investigations.

---

## 🖼️ Screenshots



---

## ✅ Final Takeaway
