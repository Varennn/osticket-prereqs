<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />
For this demonstration, I will be using an older verion than the current release so always make your you use the most up to date installation files!<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- PHP Manager for IIS installatiion file. Filename example: (PHPManagerForIIS_v1.5.0.msi)
- Rewrite Module. Filename example: (rewrite_amd64_en-US.msi) 
- PHP 7.3.8. Filename example (9php-7.3.8-nts-Win32-VC15-x86.zip)
- VC_redist.x86.exe
- MySQL 5.5.62 Filename example:(mysql-5.5.62-win32) 
- Heidi SQL Filename example (HeidiSQL_12.3.0.6589_Setup.exe)

<h2>Installation Steps</h2>

<p>
Navagate to Control Panel - Programs - Turn WIndows Feteatures on or off.
</p>

<p>
<img src="https://i.imgur.com/a6hyXrT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Under the windows features window, navagate to the Internet information services folder, check the box and continue into Web Management Tools, and check the box for IIS Management Console.
There is a folder below that called World Wide Web Services, open that and navagate to Common HTTP Features, check all the boxes in this folder. It should look like this after.
</p>
<br />

<p>
<img src="https://i.imgur.com/yk8ESVs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
From the Prerequisite files install the PHP Manager for IIS installatiion file. Filename example: (PHPManagerForIIS_v1.5.0.msi)
Do the same with the Prerequisite file Rewrite Module. Filename example: (rewrite_amd64_en-US.msi) and install it.
</p>
<br />

<p>
Now you need to create a folder named PHP in your C Directory with the file address of C:\PHP.
</p>

From the Prerequisite files, find the file PHP 7.3.8 Filename example (9php-7.3.8-nts-Win32-VC15-x86.zip), rightclick and click Extract all, select the folder you created named PHP, and extract into that folder. 
</p>

<p> 
From the Prerequisite files install the VC_redist.x86.exe
</p>

<p> 
From the Prerequisite files install MySQL 5.5.62 Filename example:(mysql-5.5.62-win32) select Typical Setup and check the box after installation that says Launch the MySQL Instance Configuration Wizard.
</p>

<p>
<img src="blob:https://imgur.com/03d6f6f8-4b16-4573-8dac-454611171a25" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
