# Configuring-Active-Directory-within-Azure
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

1. __Set Up the Environment__
- Prepare the required infrastructure, systems, and tools.
2. __Deploy Active Directory__
- Install and configure Microsoft Azure Directory on a server.
3. __Integrate Active Directory with Azure AD__
- Use Azure Ad to connect and sync the on-premises Active Directory with Azure AD.
4. __Test and validate Configuration__
Verify successful synchronization and user authentication between environments. 
     
- Joint Client-1 to the domain. On Client-1, Navigate to __System Properties__ > __Computer name__ > __Change__ and join it to the Domain. 
- We can now create __Organizational Units (OUs)__, add __users__ and __groups__, and set up __Group Policy Objects__

<h2>Deployment and Configuration Steps</h2>


  __Step 1: Set Up Domain Controller (DC-1)__ 
  1. Create a Virtual Machine:
-  Login to the Azure Portal and create a new virtual machine (VM) using Windows Server 2022 as the image.
-  Assign the VM a private IP address in your chosen virtual network (VNET).
  2. Configure the NIC settings:
- Navigate to the Networking tab for DC-1 in the Azure portal.
- Select the NIc and set the private IP address to static. This ensures the IP address remains consistent for the domain controller.
3. Promote DC-1 to a Domain Controller:
- Log in to the DC-1 Vm via Remote Desktop (RDP).
-  Open Server Manager, select Add roles and features, and install the Active Directory Domain Services role. 
-  Promote the server to a domain controller and create a new forest.
>

    **screenshot server manager- installing adds role**
  
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
