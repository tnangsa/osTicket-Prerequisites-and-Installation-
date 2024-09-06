<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create an Azure Virtual Machine, Windows 10, 4 vCPUs 1
- Install and enable IIS in Windows (CGI & HTTP Features)
- Register PHP within IIS
- Install and configure osTicket
- Install HeidiSQL and complete osTicket

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
The image above shows all the prerequisites that were downloaded to begin our installation of osTicket. The following are the steps to take to install osTicket successfully:

- A virtual machine created in Azure with 2-4 Virtual CPUs
- Install and enable IIS in Windows with CGI and Common HTTP features
- Install PHP manager for IIS, Rewrite Module, PHP 7.3.8, VC_redist.x86.exe, and MySQL 5.5.62
- Created a directory for PHP on the C drive
  
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

In this step, I registered PHP from within IIS. Here are the steps that were taken:

- Open IIS as an administrator (go to start menu and search IIS and then right-click to run as an administrator)
- Select PHP manager
- Register new PHP version: Go to the C drive to register with PHP we created in our first few steps
- Reload IIS (either end and start the server or just restart it)
  
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The above image shows the completed installation of osTicket v1.15.8 following the final steps in our installation process from our prerequisites.

- Install the osTicket file
- Extract and copy the "upload" folder to C:\inetpub\wwwroot
- Go into C:\inetpub\wwwroot and rename "upload" to "osTicket"
- Reload IIS and restart the server
- On IIS, select "Browse *:80"
- Add extensions that are not enable, follow these steps to do so:
    - Go to IIS > sites > default > osTicket
    - Double click PHP manager
    - Select "Enable or disable an extension"
        - Enable: php_imap.dll
        - Enable: php_intl.dll
        - Enable: php_opcache.dll
        - Refresh the osTicket site browser, observe the changes
- Rename: ost-config.php
- Assign Permissions: ost-config.php
- Continue setting up osTicket in the browser
- Install HeidiSQL
- Complete installation of osTicket in the browser  


</p>
<br />
