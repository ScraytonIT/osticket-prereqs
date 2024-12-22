<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Deploy osTicket virtual machine and network
- Install osTicket installation file; unzip/extract file
- Enable Information Internet Services(IIS) with CGI; multiple folders will be accessed here
- Install and launch MySQL Server; create username and password
- Install HeidiSQL

<h2>Installation Steps</h2>

<p>
<img width="1139" alt="Screenshot 2024-12-22 at 11 20 49 AM" src="https://github.com/user-attachments/assets/cf68bc9a-6686-4880-83cc-54ecf9aebf04" />

</p>
<p>
Step 1: Create and Prepare the Virtual Machine
Create an Azure Virtual Machine (VM) with the following details:
Name: osticket-vm, OS: Windows 10, Specs: 4 vCPUs, Create Username & Password,
Use Remote Desktop to log into the VM.
Download and unzip the osTicket-Installation-Files.zip onto the VM’s desktop into a folder named osTicket-Installation-Files.
</p>
<br />

<p>
<img width="976" alt="Screenshot 2024-12-16 at 12 05 05 PM" src="https://github.com/user-attachments/assets/fb6139cb-76d4-4070-909c-c542b7188622" />
</p>
<p>

Step 2: Install IIS, PHP, and MySQL
Enable IIS with CGI (World Wide Web Services > Application Development Features > CGI).
From the osTicket-Installation-Files folder, install:
PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi).
Rewrite Module (rewrite_amd64_en-US.msi).
VC_redist.x86.exe and MySQL 5.5.62 (Create Username & Password).
Unzip PHP 7.3.8 into C:\PHP, then register it in IIS (PHP Manager > C:\PHP\php-cgi.exe).
Reload IIS by stopping and starting the server.

</p>
<br />
<img width="828" alt="Screenshot 2024-12-16 at 12 29 45 PM" src="https://github.com/user-attachments/assets/cdbf5423-5992-4515-b04c-12deaece00fa" />

<p>

</p>
<p>
Step 3: Install and Configure osTicket
Unzip osTicket-v1.15.8.zip, move the "upload" folder to C:\inetpub\wwwroot, and rename it to osTicket.
Enable PHP extensions in IIS (php_imap.dll, php_intl.dll, php_opcache.dll), and reload IIS.
Rename and assign permissions to ost-config.php as instructed, then set up osTicket in the browser:
Database: osTicket, Username: root, Password: root.
Finalize installation by creating a database with HeidiSQL, clean up setup files, and set permissions to "Read-Only" for ost-config.php. Access your helpdesk at http://localhost/osTicket!
</p>
<br />
