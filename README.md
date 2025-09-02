<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1: Prepare Active Directory
- Step 2: Deploy Active Directory
- Step 3: Create Users
- Step 4: Group Policy  

<h2>Deployment and Configuration Steps</h2>


<h2>Step 1: Preparing Active Directory Infrastructure In Azure</h2>

### - Create a Virtual Network 
---
<img width="1600" height="900" alt="Screenshot (19)" src="https://github.com/user-attachments/assets/d55772b5-487e-4cb0-acfe-c1ade1fe2298" />

---
### - Create 2 Virtual Machines - 1 Client Machine (Client-1) and 1 Server Machine (DC-1)

---
<img width="1600" height="900" alt="Screenshot (17)" src="https://github.com/user-attachments/assets/3dfa1612-4449-4f86-95ba-87b924cb2b47" />


---

<img width="1600" height="900" alt="Screenshot (21)" src="https://github.com/user-attachments/assets/bd6f8a1c-9a38-48cd-8086-4e52bd1a7631" />

---
### - Set the private ip address on DC-1 to static

---

<img width="1600" height="900" alt="Screenshot (20)" src="https://github.com/user-attachments/assets/24fa2734-a2e1-416f-8314-adfe52de0e5f" />


---
### - Log in to DC-1 and turn off the Windows Firewalls

---

<img width="1600" height="900" alt="Screenshot (22)" src="https://github.com/user-attachments/assets/060bacae-a942-4499-83eb-b498f42e66ca" />

---
### - Set up DNS server on Client-1 using DC-1 private ip address

---

<img width="1600" height="900" alt="Screenshot (23)" src="https://github.com/user-attachments/assets/a6517164-d384-4a6d-882f-44ca272329b3" />

---

### - Use Powershell to test setup with both ping and ipconfig commands

---

<img width="1600" height="900" alt="Screenshot (24)" src="https://github.com/user-attachments/assets/23c9d5cd-1b7d-424b-9cdb-6765eaf298a1" />

---

<img width="1600" height="900" alt="Screenshot (25)" src="https://github.com/user-attachments/assets/2019735b-1b48-42f4-a2b5-ec3e77d792c8" />

---

<h2>Step 2: Deploying Active Directory</h2>

### - Promote DC-1 as Domain Controller and set up Active Directory Domain Services
  
---

<img width="1600" height="900" alt="Screenshot (26)" src="https://github.com/user-attachments/assets/5ee9be30-733d-48ec-9f06-9015fffe9d38" />


---

<img width="1600" height="900" alt="Screenshot (27)" src="https://github.com/user-attachments/assets/6888f45c-29e9-46f3-a149-eced6b29cc5a" />

---
### - Add a new forest (mydomain.com)

---

<img width="1600" height="900" alt="Screenshot (28)" src="https://github.com/user-attachments/assets/291f86d2-4081-433e-8f10-b31a1aa74bb6" />

---

### - Create a new admin user (Jane Doe) with Active Directory Users and Computers

---

<img width="1600" height="900" alt="Screenshot (29)" src="https://github.com/user-attachments/assets/894bf2c8-733d-40c4-ad89-e47e59bcc14f" />

---

<img width="1600" height="900" alt="Screenshot (30)" src="https://github.com/user-attachments/assets/dce8cb50-2e26-41e8-b4da-ad472b056b88" />

---

### - Make Client-1 a member of mydomain.com

---

  
<img width="1600" height="900" alt="Screenshot (31)" src="https://github.com/user-attachments/assets/9524fabb-980c-451d-98b5-54801c363585" />

---

<img width="1600" height="900" alt="Screenshot (32)" src="https://github.com/user-attachments/assets/de0efa17-116a-419b-ba6f-8155c4cb942e" />

---

<h2>Step 3: Creating Users With Powershell</h2>

### - Add Domain Users to Remote Desktop Users on Client-1

---

<img width="1600" height="900" alt="Screenshot (33)" src="https://github.com/user-attachments/assets/0a61881b-dd78-47ee-984c-0894681b19fd" />

---

### - Run script in Powershell ISE on DC-1 to generate new users

---

<img width="1600" height="900" alt="Screenshot (34)" src="https://github.com/user-attachments/assets/1b48f07b-c7f2-4eda-8733-28e03a03f716" />


---

### - Test a new user account (nose.wed) and log in to Client-1

---
  
<img width="1600" height="900" alt="Screenshot (35)" src="https://github.com/user-attachments/assets/2206ac3d-3da2-4036-95c6-5d0302204d91" />

---


<img width="1600" height="900" alt="Screenshot (42)" src="https://github.com/user-attachments/assets/c804a2f0-d4eb-4771-9557-6356f768134e" />

---

<h2>Step 4: Group Policy and Managing Accounts</h2>

### - Use Group Policy Management (gpmc.msc) to set up Account Lockout Policy

---


<img width="1600" height="900" alt="Screenshot (36)" src="https://github.com/user-attachments/assets/34af0a1c-964d-4cb8-be65-8f18c8579f6c" />


---

### - Trigger a lockout and unlock the user account

---

<img width="1600" height="900" alt="Screenshot (37)" src="https://github.com/user-attachments/assets/050df9ef-987e-4a4a-aea2-6abe38043649" />


---

<img width="1600" height="900" alt="Screenshot (38)" src="https://github.com/user-attachments/assets/4f8ac407-d5af-4910-80ca-00641995f28b" />

---

### - Disable/Enable user account in Active Directory Users and Computers

---

<img width="1600" height="900" alt="Screenshot (39)" src="https://github.com/user-attachments/assets/192b9e7e-186c-441a-9ab0-10afb3e024c7" />

---

<img width="1600" height="900" alt="Screenshot (40)" src="https://github.com/user-attachments/assets/368a787c-9b71-4c5d-a7d6-ef5a50b5bbb2" />


---

### - View security logs in Event Viewer for the account lockout that we triggered

---

<img width="1600" height="900" alt="Screenshot (41)" src="https://github.com/user-attachments/assets/4f1294b2-7252-4086-b64f-b825d06796d8" />

---



</p>
<br />
