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

1. __Deploy a Virtual Machine (VM)__
2. __Deploy Active Directory__
3. __Create Organizational Units (OUs) and Manage Users__
4. __Set up Group Policies__

     


<h2>Deployment and Configuration Steps</h2>

__Step 1:Set up the environment__ 
* Go to the Azure portal and click __Create a Resource__.
*  Select __Virtual Machine__ and configure the following:
     *  Select Windows Server 2022 as your image.
     *  Set username, password, and resource group.
     *  Ensure the VM is deployed in a virtual network.
* Start the Vm and connect to it via __RDP__.    
   



  
<img src="https://github.com/diegomtz28/Configuring-Activer-Directory-within-Azure/blob/main/Vm%20Deployed%20(DC-1).png"/>


__Step 2: Deploy Active Directory__
* Once connected to the VM:
     * Open Server Manager and install the __AD DS role__. 
     *  Promote the server to a domain controller and create domain.
**(The ad ds innstalation in server manager)**




<img src="https://github.com/diegomtz28/Configuring-Activer-Directory-within-Azure/blob/main/Deploying%20Active%20Directory.png"/>

__Step 3: Create Organization Units (OUs) and Users__
* Open Active Directory Users and Computers on the Azure VM.
* Create a new OU
* Add users to the domain and assign them to the OU.


<img src="https://github.com/diegomtz28/Configuring-Activer-Directory-within-Azure/blob/main/OU%20and%20User%20Accounts.png"/>


__Step 4: Set up Grouop Policies__
* Open __Group Policy Managment__.
* Create a __Group Policy Object (GPO)__ and link it to an OU.
* Configure simple policies (enforcing passwords or a desktop wallpaper)

  <img src="https://github.com/diegomtz28/Configuring-Activer-Directory-within-Azure/blob/main/Linking%20Group%20Policy%20to%20OU.png"/>

__Step 5: Test Active Directory Fuinctionality__
- create another VM in azure (Windows 10) in the same Virtual Network.
- Join the new VM to the domain.
- Log in a one of the domain users created earlier.

  **(Confirmation of the client vm joining the domain, successful login as a domain user.**
  <img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br />

