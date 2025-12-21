# 🎄Advent of Cyber 2025 – Day 20🎄
### Race Conditions - Toy to The World

---

## 🎯 Objective 

The objective of Day 20 was to understand what a race condition is and how it can be exploited in a web application.
By observing how the checkout process worked and then abusing timing issues with multiple simultaneous requests, I learned how attackers can bypass logic checks and cause unintended behavior such as overselling limited items.

---

## 🛠 Tools & Techniques Used



---

## 🧠 What I Learned Today

- Race conditions happen when multiple actions occur at the same time without proper synchronization
- Applications can behave incorrectly if checks and updates are not atomic
- Limited-stock items are common targets for race condition attacks
- Burp Repeater can be used to send multiple requests simultaneously
- Even “normal” functionality can become vulnerable under timing pressure

---

## 📌 Step-by-Step Summary

**1.** Scanned the target system to identify exposed services

**2.** Logged into the web application using provided credentials

**3.**Made a legitimate purchase to observe normal behavior

**4.** Captured the checkout request using Burp Proxy

**5.** Sent the checkout request to Burp Repeater

**6.** Duplicated the request multiple times

**7.** Sent all requests in parallel to exploit the race condition

**8.** Observed multiple successful purchases despite limited stock

**9.** Confirmed exploitation by viewing updated stock and flag
  
---

## 🔐 Key Cybersecurity Concepts

- Race Condition – When system behavior depends on timing between actions
- TOCTOU (Time-of-Check to Time-of-Use) – Data changes between validation and execution
- Atomic Operations – Actions that must complete fully or not at all
- Concurrency Issues – Problems caused by simultaneous requests
- Web Application Logic Flaws – Vulnerabilities in how applications handle state

---

## 🖼️ Screenshots

For this task, I decided to intentionally leave out the screenshots.
The vulnerability focused on application logic and timing rather than visible interface changes.
The investigation and exploitation steps are therefore documented in text to better explain the reasoning and behavior observed during the attack.

![day 20 complete](screenshots/Day19-completed.png)

*Proof of completing Day 20.* ⬆️

---

## 🧭 Investigation Approach

I first tried to understand how the website was meant to work normally.
Instead of attacking it right away, I made a normal purchase to see how the stock system behaved and when the stock number was updated.
After that, I looked at the checkout request and how the server handled several requests at the same time.
By sending the same checkout request multiple times in parallel, I noticed that the stock check didn’t update fast enough, which allowed more purchases than should be possible.
Taking it step by step helped me understand what went wrong in the system, instead of just exploiting it without knowing why it worked.

---

## ✅ Final Takeaway

Day 20 showed me that security problems don’t always come from advanced hacking techniques.
Even small timing issues in normal website features can cause big problems if they aren’t handled properly.
Race conditions are a good example of how mistakes in logic can be just as dangerous as more obvious security bugs.
This challenge helped me understand why it’s important for applications to handle actions in the correct order and not assume things will always happen one at a time.
