# 🎄Advent of Cyber 2025 – Day 23🎄
### AWS Security - S3cret Santa

---

## 🎯 Objective 

The goal of today’s task was to learn the basics of AWS enumeration, focusing on how misconfigured IAM permissions can lead to unintended access to sensitive resources such as S3 buckets. The task demonstrated how attackers (or defenders testing security) can move from limited access to broader permissions.

---

## 🛠 Tools & Techniques Used

- AWS CLI – to interact with AWS services using credentials
- IAM enumeration – inspecting users, policies, and roles
- STS (Security Token Service) – assuming roles to gain temporary permissions
- S3 enumeration – listing buckets and accessing objects
- Cloud security mindset – understanding misconfigurations and privilege escalation

---

## 🧠 What I Learned Today

- IAM permissions are often the weakest link in cloud security
- Even limited permissions (like listing users or roles) can be useful to attackers
- Inline policies and role trust relationships can expose unintended access
- The sts:AssumeRole permission is especially powerful
- Misconfigured S3 buckets can lead to data exposure
- Enumeration is often a slow, step-by-step process rather than a single exploit

---

## 📌 Step-by-Step Summary

I started by using the AWS CLI to enumerate the current IAM user and understand what permissions were available. From there, I listed user policies and confirmed that the user had permission to enumerate IAM entities but not much else directly.
Next, I discovered that the user was allowed to assume an IAM role. By enumerating available roles, I found a role that trusted the current user. I inspected the role’s policy and noticed it had permissions related to S3 access.
Using AWS STS, I assumed the role and received temporary credentials. After setting these credentials in the environment, I confirmed that the role was successfully assumed.
With the new permissions, I enumerated S3 buckets, found an interesting bucket, listed its contents, and finally downloaded an object from it. This showed how a small IAM misconfiguration could lead to sensitive data exposure.
  
---

## 🔐 Key Cybersecurity Concepts

- IAM (Identity and Access Management): Controls who can do what in AWS
- Least privilege: Users and roles should only have permissions they actually need
- Role assumption: Temporarily gaining permissions via trusted roles
- STS: AWS service that issues temporary credentials
- S3 misconfiguration: A common cause of cloud data leaks
- Cloud enumeration: Discovering available resources and permissions

---

## 🖼️ Screenshots


![day 23 complete](screenshots/day22-completed.png)

*Proof of completing Day 23.* ⬆️

---

## 🧭 Investigation Approach

I approached this task with a learning-focused mindset, taking time to understand what the current credentials allowed rather than assuming immediate access. I paid close attention to IAM policies and role trust relationships, as these often reveal unexpected access paths. When new permissions were gained, I verified each step before moving forward, focusing on understanding how the access escalation happened instead of rushing to the final result.

---

## ✅ Final Takeaway

This task showed how small IAM misconfigurations can have big consequences in cloud environments. Even when an account seems locked down, permissions like role assumption or basic enumeration can open unexpected paths to sensitive data. For cloud security, this highlights why regular IAM reviews, least privilege, and monitoring role usage are critical.
