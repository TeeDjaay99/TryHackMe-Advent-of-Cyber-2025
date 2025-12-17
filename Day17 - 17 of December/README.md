# 🎄Advent of Cyber 2025 – Day 17🎄
### CyberChef - Hoperation Save McSkidy

---

## 🎯 Objective 

The objective of Day 17 was to analyze a web-based challenge where login credentials were hidden using different encoding and transformation techniques. By inspecting web pages and reversing encoded data with CyberChef, the goal was to break through multiple security layers and ultimately rescue McSkidy.

---

## 🛠 Tools & Techniques Used

- CyberChef
  - Base64 encoding/decoding
  - XOR operations
  - ROT-based transformations
  - Chained decoding recipes

- Browser Developer Tools
  - Network tab (headers and responses)
  - Debugger tab (JavaScript login logic)

- Basic hash analysis
  - Understanding when hashes cannot be reversed directly

- Logical analysis
  - Matching observed behavior with decoding techniques

---

## 🧠 What I Learned Today

- Encoding is not encryption and can often be reversed if you understand the logic.
- Web applications may expose useful information in headers or client-side JavaScript.
- CyberChef is extremely powerful when decoding steps are chained together.
- Each challenge may reuse similar techniques but apply them differently, so assumptions can easily lead to mistakes.
- Reading and understanding logic is more important than blindly trying tools.

---

## 📌 Step-by-Step Summary

**1.** Opened the target web application and identified encoded data shown by the guard.

**2.** Used browser developer tools to inspect:
  - Page headers
  - Network responses
  - JavaScript login logic

**3.** Identified which encoding or transformation methods were used for each lock.

**4.** Reversed the logic step by step using CyberChef by chaining the correct operations.

**5.** Adjusted the decoding process when the logic changed between different locks.

**6.** Repeated the investigation process until all locks were bypassed and McSkidy was rescued.
  
---

## 🔐 Key Cybersecurity Concepts

**Encoding vs Encryption**
Encoding is meant for data formatting and can usually be reversed, while encryption is designed to protect confidentiality.

**Client-Side Logic Exposure**

Sensitive logic implemented in client-side JavaScript can often be inspected and abused.

**Chained Transformations**

Attackers may combine multiple encoding methods to slow down analysis.

**Hash Awareness**

Some hashes cannot be reversed directly and require alternative approaches such as hash lookups.

**Logic-Based Attacks**

Understanding how data is transformed is often more important than the tools used.

---

## 🖼️ Screenshots


![registry explorer](screenshots/01-.png)


![registry explorer](screenshots/01-.png)


![registry explorer](screenshots/01-.png)


---

## ✅ Final Takeaway

Day 17 showed that breaking security challenges is not about guessing or brute force — it’s about understanding logic. By carefully inspecting how data was transformed and reversing it step by step, even complex-looking protections became manageable. This task showed the importance of patience, analysis, and trying to think like an attacker.
