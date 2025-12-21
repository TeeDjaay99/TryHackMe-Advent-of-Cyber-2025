# 🎄Advent of Cyber 2025 – Day 19🎄
### ICS/Modbus - Claus for Concern

---

## 🎯 Objective 

The objective of Day 19 was to understand how industrial control systems (ICS) work and how insecure protocols like Modbus TCP can be abused to manipulate real-world processes.
By interacting directly with a PLC using Python, I practiced identifying misconfigurations, understanding system logic, and safely restoring a compromised control system.

---

## 🛠 Tools & Techniques Used

- Nmap (service discovery)
- Modbus TCP (port 502)
- Python
- pymodbus library
- PLC register & coil analysis
- Static and live system observation (CCTV feed)
- Safe remediation techniques

---

## 🧠 What I Learned Today

- SCADA and PLCs control physical processes, not just data
- Modbus TCP has no authentication or encryption by default
- Anyone with network access can read or change PLC values
- Registers and coils control critical system behavior
- Changing values in the wrong order can trigger safety traps
- Always understand system logic before attempting remediation

---

## 📌 Step-by-Step Summary

**1.** Learned how SCADA systems, PLCs, and Modbus work together

**2.** Identified exposed services using Nmap

**3.** Connected directly to the PLC via Modbus TCP (port 502)

**4.** Read holding registers to understand system configuration

**5.** Read coils to identify safety mechanisms and traps

**6.** Discovered a protection mechanism designed to punish careless changes

**7.** Created a reconnaissance script to inspect the full system state

**8.** Carefully restored the system by following the correct order of changes
  
---

## 🔐 Key Cybersecurity Concepts

- ICS / SCADA – Systems that control industrial processes
- PLC (Programmable Logic Controller) – Executes real-time control logic
- Modbus TCP – Industrial protocol with no built-in security
- Holding Registers – Writable numeric configuration values
- Coils – Boolean control flags (on/off)
- Logic manipulation – Attacking behavior instead of availability
- Safe remediation – Fixing systems without triggering safeguards

---

## 🖼️ Screenshots



---

## 🧭 Investigation Approach

I started by reading the task instructions carefully to understand how industrial systems work compared to normal IT systems.
Instead of changing values right away, I first watched how the system behaved using the CCTV feed and by checking the PLC registers and coils.
After I understood how package types, delivery zones, and safety mechanisms were connected, I planned my changes before touching anything.
This helped me avoid triggering the self-destruct trap and allowed me to fix the system safely by changing values in the correct order.

---

## ✅ Final Takeaway

Day 19 showed how dangerous insecure industrial protocols can be when exposed to networks.
Even simple changes to numeric values can cause serious real-world consequences if the system logic isn’t understood.
