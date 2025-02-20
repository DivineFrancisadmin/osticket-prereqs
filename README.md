<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Setup
- Install IIS (Internet Information Services) with CGI
- Install Required Software & Dependencies
- Configure IIS and PHP
- Set Up osTicket and Database

<h2>Installation Steps</h2>

<p> Azure Virtual Machine Setup for osTicket Installation

  ![1  Azure-vm-setup](https://github.com/user-attachments/assets/fc191809-4643-416f-8857-32039e4c9631)

<p>
To set up my Azure Virtual Machine for osTicket, I started by creating a Windows 10 VM in the Azure Portal with 2 vCPUs. I named it osticket-vm and set my credentials as Username: labuser and Password: osTicketPassword1!. After the VM was deployed, I enabled Remote Desktop (RDP) by going to the Networking section in Azure and allowing RDP (Port 3389) under inbound rules. Then, on my local PC, I opened the Microsoft Remote Desktop app from the Windows Store, entered my VM’s public IP address, and logged in using my credentials. This gave me remote access to manage my virtual machine.
</p>
<br />

<p>
<img width="1135" alt="2  IIS-CGI" src="https://github.com/user-attachments/assets/3b3cef2f-2f8d-4aab-a78b-d190908f2d22" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
