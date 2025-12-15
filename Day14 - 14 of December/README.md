# 🎄Advent of Cyber 2025 – Day 14🎄
### Containers - DoorDasher's Demise

---

## 🎯 Objective 

The objective was to investigate a containerized environment, identify how a compromised service was abused, and restore a defaced web application.
This challenge focused on understanding Docker containers, container escape risks, and how misconfigurations—especially exposed Docker sockets—can lead to full system compromise.

---

## 🛠 Tools & Techniques Used

- Docker CLI (docker ps, docker exec)
- Linux command line
- Container inspection
- Privilege escalation via Docker socket access
- Basic incident response and service recovery

---

## 🧠 What I Learned Today

Today helped me understand a little more how containers work in practice and why they are powerful—but also dangerous if misconfigured.
Containers are lightweight and share the host operating system, which makes them fast and scalable, but this also means that mistakes like exposing the Docker socket can allow attackers to escape containers and gain full control of the host.
I also learned how attackers can abuse internal services rather than exploiting traditional software vulnerabilities.

---

## 📌 Step-by-Step Summary

**1.** Identified running Docker containers using `docker ps`

**2.** Accessed the main web application and confirmed it was defaced

**3.** Entered the `uptime-checker` container to investigate further

**4.** Discovered that the Docker socket (`/var/run/docker.sock`) was exposed

**5.** Used Docker access to enter a privileged container

**6.** Gained root-level access inside the container environment

**7.** Executed a recovery script to restore the original web application

**8.** Verified that the service was successfully restored
  
---

## 🔐 Key Cybersecurity Concepts

**Containers vs Virtual Machines**
  - Containers share the host OS kernel and isolate applications only
  - Virtual machines include a full guest OS and stronger isolation

**Docker Socket Exposure**
  - The Docker socket allows direct control of the Docker daemon
  - If accessible inside a container, it can lead to full host compromise

**Container Escape**
  - Attackers can move from a container to the host system
  - Often caused by misconfigurations rather than software bugs

**Principle of Least Privilege**
  - Containers should never have more permissions than necessary
  - Internal tools should not be exposed to untrusted containers

---

## 🖼️ Screenshots




---

## ✅ Final Takeaway

This challenge showed me that containers are very useful, but they can also be dangerous if they are not set up correctly.
A single exposed Docker socket was enough to take control of the whole system, which shows how small mistakes can lead to big security problems.
Understanding these risks is important when working with cloud systems, containers, and incident response, especially in modern environments where containers are used everywhere.
