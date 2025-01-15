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
- Verify successful synchronization and user authentication between environments. 
     


<h2>Deployment and Configuration Steps</h2>

__Step 1:Set up the environment__ 
* Create a virtual machine (VM) using Windows Server 2022
*  Install necessary tools like Powershell and Azure AD connect.
*  Ensure network connectivity and proper firewall configurations for Azure synchronization.


    **screenshot server manager- installing adds role**
  
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


__Step 2: Deploy Active Directory__
*  Install the Active Directory Domain Services (AD DS) role on the server.
*  Promote the server to a domain controller.
*  create organizational units (OU's), users, and groups for role management.





<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

__Step 3: Integrate Active Directory with Azure AD__
* Install and configure Azure AD Connect on the domain controller.
* Select synchronization options
*  Configure filters to limit which objects are synced. 
* Verify Synchronization of users, groups, and attributes in the Azure Portal.

<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


__Step 4:__ Test and Validate Configuration
* Log in to Azure Ad with on-premise AD credentials to confirm synchronization.
* Validate users and groups appear in Azure Ad as expected
* Test any additional functionality, such as SSO or MFA, if implemented.

  <img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
