# 🖥️ Windows Server Exam LAB (1)

## 📌 Lab Overview
This lab demonstrates the deployment and configuration of an **Active Directory Domain Services (AD DS)** environment on Windows Server, including Group Policy, user and group management, and client integration.  

**Domain Name:** `zohdy.local`  
**Server Name:** `PDC-SRV`  
**Server IP:** `192.168.1.2`  
**Client Name:** `PC-01`  
**Client IP:** `192.168.1.50`  

---

## ⚙️ Configuration Steps

### 1. Domain Setup
- Installed **Active Directory Domain Services** on `PDC-SRV`.  
- Promoted server to Domain Controller with domain name `zohdy.local`.

### 2. Organizational Units (OUs)
Created separate OUs for departments:
- **HR**
- **Sales**
- **IT**

### 3. User Accounts
Created sample users in each OU:
- HR: `Mohamed Zohdy`, `Salma Mohamed`
- Sales: `Alaa Kamal`
- IT: `Ahmed Nabil`

### 4. Groups
- Created separate security groups for each department.  
- Added department users to their respective groups.

### 5. Client Join
- Joined client machine `PC-01` with IP `192.168.1.50` to the domain `zohdy.local`.

### 6. Group Policy Objects (GPOs)
Applied different GPOs as required:
- **HR & Sales**
  - Remove *Programs and Features* from Control Panel.  
  - Remove *Properties* from This PC context menu.  
  - Disable *Command Line* and *Run*.  
  - Disable *External Storage* (USB).  
- **HR (Custom)**
  - HR Manager `Mohamed Zohdy` excluded from USB restriction.  
  - HR users receive shortcut `http://hrapp.zohdy.local` on Desktop.  
- **IT**
  - Excluded from Task Manager restriction.  
- **Domain-wide Policies**
  - Disabled *Task Manager* for all users except IT.  
  - Password Policy:
    - Change every 90 days.  
    - Minimum length: 4 digits.  
    - Remember last 2 passwords.  
    - Lock account for 60 mins after 5 failed attempts.  
  - Created local admin user `itadmin` on all domain computers.  
  - Added `IT-Group` as Local Administrators on client machines.  
  - Allowed **ICMP (Ping)** traffic in Windows Firewall.  

---

## 🖼️ Screenshots
https://github.com/Abdallahreda97/Windows-Server-Exam-LAB-2-/blob/main/Screenshots/Ad-Project_Exam2-0.png
https://github.com/Abdallahreda97/Windows-Server-Exam-LAB-2-/blob/main/Screenshots/Ad-Project_Exam2-1.png
https://github.com/Abdallahreda97/Windows-Server-Exam-LAB-2-/blob/main/Screenshots/Ad-Project_Exam2-2.png
https://github.com/Abdallahreda97/Windows-Server-Exam-LAB-2-/blob/main/Screenshots/Ad-Project_Exam2-3.png
https://github.com/Abdallahreda97/Windows-Server-Exam-LAB-2-/blob/main/Screenshots/Ad-Project_Exam2-4.png
https://github.com/Abdallahreda97/Windows-Server-Exam-LAB-2-/blob/main/Screenshots/Ad-Project_Exam2-5.png
https://github.com/Abdallahreda97/Windows-Server-Exam-LAB-2-/blob/main/Screenshots/Ad-Project_Exam2-6.png
https://github.com/Abdallahreda97/Windows-Server-Exam-LAB-2-/blob/main/Screenshots/Ad-Project_Exam2-7.png
https://github.com/Abdallahreda97/Windows-Server-Exam-LAB-2-/blob/main/Screenshots/Ad-Project_Exam2-8.png
https://github.com/Abdallahreda97/Windows-Server-Exam-LAB-2-/blob/main/Screenshots/Ad-Project_Exam2-9.png
https://github.com/Abdallahreda97/Windows-Server-Exam-LAB-2-/blob/main/Screenshots/Ad-Project_Exam2-10.png
https://github.com/Abdallahreda97/Windows-Server-Exam-LAB-2-/blob/main/Screenshots/Ad-Project_Exam2-11.png
https://github.com/Abdallahreda97/Windows-Server-Exam-LAB-2-/blob/main/Screenshots/Ad-Project_Exam2-12.png
https://github.com/Abdallahreda97/Windows-Server-Exam-LAB-2-/blob/main/Screenshots/Ad-Project_Exam2-13.png
https://github.com/Abdallahreda97/Windows-Server-Exam-LAB-2-/blob/main/Screenshots/Ad-Project_Exam2-14.png
https://github.com/Abdallahreda97/Windows-Server-Exam-LAB-2-/blob/main/Screenshots/Ad-Project_Exam2-15.png
---

## ✅ Summary
This project covered:
- Domain setup and promotion.  
- OU structure per department.  
- User and group creation.  
- Joining a client machine to the domain.  
- Applying tailored GPOs for HR, Sales, and IT.  
- Implementing security baselines (password policy, account lockout).  
- Firewall and local admin group configurations.  

---
