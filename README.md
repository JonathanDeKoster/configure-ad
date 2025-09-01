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

- Create a Virtual Network 

<img width="1600" height="900" alt="Screenshot (19)" src="https://github.com/user-attachments/assets/d55772b5-487e-4cb0-acfe-c1ade1fe2298" />

- Create 2 Virtual Machines - 1 Client Machine (Client-1) and 1 Server Machine (DC-1)
<img width="1600" height="900" alt="Screenshot (17)" src="https://github.com/user-attachments/assets/3dfa1612-4449-4f86-95ba-87b924cb2b47" />




<img width="1600" height="900" alt="Screenshot (21)" src="https://github.com/user-attachments/assets/bd6f8a1c-9a38-48cd-8086-4e52bd1a7631" />


- Set the private ip address on DC-1 to static

<img width="1600" height="900" alt="Screenshot (20)" src="https://github.com/user-attachments/assets/24fa2734-a2e1-416f-8314-adfe52de0e5f" />


Log in to DC-1 and turn off the Windows Firewalls

<img width="1600" height="900" alt="Screenshot (22)" src="https://github.com/user-attachments/assets/060bacae-a942-4499-83eb-b498f42e66ca" />

- Set up DNS server on Client-1 using DC-1 private ip address

<img width="1600" height="900" alt="Screenshot (23)" src="https://github.com/user-attachments/assets/a6517164-d384-4a6d-882f-44ca272329b3" />


- Use Powershell to test setup with both ping and ipconfig commands

<img width="1600" height="900" alt="Screenshot (24)" src="https://github.com/user-attachments/assets/23c9d5cd-1b7d-424b-9cdb-6765eaf298a1" />



<img width="1600" height="900" alt="Screenshot (25)" src="https://github.com/user-attachments/assets/2019735b-1b48-42f4-a2b5-ec3e77d792c8" />




<h2>Step 2: Deploying Active Directory</h2>














<h2>Step 3: Creating Users With Powershell</h2>








<h2>Step 4: Group Policyand Managing Accounts</h2>





</p>
<br />
