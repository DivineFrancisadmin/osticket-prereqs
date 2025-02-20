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

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Setup
- Enable IIS (Internet Information Services) with CGI
- Install Required Software & Dependencies
- Configure IIS and PHP
- Set Up osTicket and Database

<h2>Installation Steps</h2>

<p> Azure Virtual Machine Setup for osTicket Installation

  ![1  Azure-vm-setup](https://github.com/user-attachments/assets/fc191809-4643-416f-8857-32039e4c9631)

<p>
To set up my Azure Virtual Machine for osTicket, I started by creating a Windows 10 VM in the Azure Portal with 2 vCPUs. I named the VM osticket-vm and set my credentials as Username: labuser and Password: osTicketPassword1!. Once the VM was deployed, I enabled Remote Desktop (RDP) for access. After configuring RDP, I switched to my local PC and opened the Windows Remote Desktop app from the App Store. I entered my VM’s public IP address and logged in using my credentials, successfully gaining remote access to manage my virtual machine. Once inside the VM, I downloaded the osTicket-Installation-Files.zip and extracted it to my desktop, to which it automatically renamed the folder to “osTicket-Installation-Files” to prepare for the installation process.
</p>
<br />
Enable IIS (Internet Information Services) with CGI
<img width="1135" alt="2  IIS-CGI" src="https://github.com/user-attachments/assets/3b3cef2f-2f8d-4aab-a78b-d190908f2d22" />
</p>
<p>
After successfully connecting to my Azure Virtual Machine via Remote Desktop, I proceeded to enable IIS with CGI to prepare for the osTicket installation. I started by opening the Control Panel, then navigated to Programs and Features and selected Turn Windows features on or off. From there, I expanded Internet Information Services (IIS) and then World Wide Web Services. Under Application Development Features, I checked the box for CGI to enable it. Once selected, I clicked OK and waited for Windows to apply the changes. This step ensured that IIS was properly configured with CGI support for the upcoming osTicket setup.</p>
<br />
<p>
Install Required Software & Dependencies
<p></p>
<img width="498" alt="3d  MySQL-install" src="https://github.com/user-attachments/assets/856bf4c5-43c7-43d3-a415-664a71ed6d49" />
<p>
  After enabling IIS with CGI, I proceeded with installing the necessary dependencies for osTicket. First, I installed PHP Manager for IIS by running PHPManagerForIIS_V1.5.0.msi from the osTicket installation folder. Next, I installed the Rewrite Module using rewrite_amd64_en-US.msi, which helps with URL rewriting in IIS. Then, I installed the Microsoft VC++ Redistributable (VC_redist.x86.exe), which is required for PHP and MySQL to function properly. After that, I created a directory at C:\PHP and unzipped PHP 7.3.8 into this location. Finally, I installed MySQL 5.5.62, ensuring that I set the username as root and the password as root. These steps prepared my environment for running osTicket smoothly on my virtual machine.
<p>
<br />
Configure IIS and PHP
</p>
<img width="1065" alt="4  PHP Registration" src="https://github.com/user-attachments/assets/7dcea664-90ce-4c6c-b17b-99a505433be6" />
<p>
 To configure IIS and PHP on my Azure Virtual Machine, I first registered PHP in IIS by opening PHP Manager and setting the path to C:\PHP\php-cgi.exe. After registering PHP, I needed to reload IIS to apply the changes. I did this by stopping and then restarting the IIS server. Once IIS was reloaded, I enabled the necessary PHP extensions by going back into PHP Manager, selecting “Enable or disable an extension”, and enabling php_imap.dll, php_intl.dll, and php_opcache.dll. These steps ensured that PHP was correctly set up and fully functional for running osTicket. 
</p>

