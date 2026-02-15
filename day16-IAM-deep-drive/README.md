# 🔐 Day 16 - AWS IAM Deep Dive

## 📌 Objective
Understand AWS Identity and Access Management (IAM) by creating users, groups, custom policies, and testing permission boundaries including explicit deny behavior.

---

## 🛠️ Services Used
- AWS IAM
- Amazon EC2
- Custom IAM Policy (JSON)
- IAM Groups
- IAM Roles

---

## 🔥 What Was Implemented

### 1️⃣ Created ReadOnly IAM User
- Created IAM user: `readonly-user`
- Attached policy: AmazonEC2ReadOnlyAccess
- Verified limited access to EC2
- Confirmed launch attempt resulted in **Access Denied**

---

### 2️⃣ Created Custom EC2 Launch Policy
- Created custom policy using JSON
- Allowed:
  - ec2:RunInstances
  - ec2:Describe*
  - ec2:CreateSecurityGroup
  - ec2:CreateKeyPair
  - ec2:CreateTags

- Created IAM Group: `ec2-launch-group`
- Attached custom policy to group
- Added user: `ec2-launch-user`

---

### 3️⃣ Tested EC2 Launch
- Logged in as `ec2-launch-user`
- Successfully launched EC2 instance
- Verified instance state = Running

---

### 4️⃣ Tested Explicit Deny
- Updated policy to add:
  - Deny: ec2:TerminateInstances
- Attempted instance termination
- Verified **Access Denied**
- Confirmed Explicit Deny overrides Allow

---

### 5️⃣ Cleanup
- Logged in as admin/root user
- Terminated EC2 instance
- Ensured no running resources to avoid charges

---

## 🧠 Key Learnings
- IAM follows strict permission evaluation logic
- Explicit Deny always overrides Allow
- EC2 launch requires multiple dependent permissions
- Roles are preferred over IAM users for services
- Root account should not be used for daily tasks

---

## 📷 Screenshots Taken
- ReadOnly Access Denied error
- Custom Policy JSON
- EC2 Launch Success
- Terminate Instance Denied error
- IAM Role creation

---

## 🎯 Outcome
Completed hands-on IAM security implementation with real-world permission testing and troubleshooting.
