<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />
For this demonstration, I will be using an older verion than the current release so always make your you use the most up to date installation files!<br />
To do this you will need to download some prerequiset files listed below.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- PHP Manager for IIS installatiion file. (Filename example: PHPManagerForIIS_v1.5.0.msi)
- Rewrite Module. (Filename example: rewrite_amd64_en-US.msi) 
- PHP 7.3.8. (Filename example: 9php-7.3.8-nts-Win32-VC15-x86.zip)
- VC_redist.x86.exe
- MySQL 5.5.62 (Filename example: mysql-5.5.62-win32) 
- Heidi SQL (Filename example: HeidiSQL_12.3.0.6589_Setup.exe)
- osTicket (FIlename example: osTicket-v1.15.8.zip)
<h2>Installation Steps</h2>

<p>
Navagate to Control Panel - Programs - Turn WIndows Feteatures on or off.
</p>

<p>
<img src="https://i.imgur.com/a6hyXrT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Under the windows features window, navagate to the Internet information services folder, check the box and continue into Web Management Tools, and check the box for IIS Management Console.<br />
There is a folder below that called World Wide Web Services, open that and navagate to Application development features and check the box named CGI.<br />
Go back to the Application development features folder and navagate to Common HTTP Features, check all the boxes in this folder.<br />
  It should look like this after.
</p>
<br />

<p>
<img src="https://i.imgur.com/abFNb7v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
From the Prerequisite files install the PHP Manager for IIS installatiion file. Filename example: (PHPManagerForIIS_v1.5.0.msi)<br />
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
When MySQL Instance Configuration Wizard gets launched, select standard configuration and next. 
<p>
<img src="https://i.imgur.com/3FyxW45.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
Keep the second page as it is and click next.
</p>
<br />
<p>
<img src="https://i.imgur.com/Lm1YfHI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
Set your Root password here. Do not lose this information! <br /> 
  Click next and then click Execute.
<p>
<img src="https://i.imgur.com/MvRhgmO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

  <p>
Now you want to open IIS as an admin, an easy way to do this is to click the start buttion, type IIS, you will see it appear in the list there, right click it, and select Run as admin.
</p>

<p>
<img src="https://i.imgur.com/X08PWgy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
Now you want to register PHP from within IIS.<br />
  To do this double-click PHP Manager, then click Register new PHP version.
</p>

<p>
<img src="https://i.imgur.com/7qAnStS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
Click the 3 dots and navagate to the folder you created earlier named PHP. </br>
In there you will find a executable file named php-cgi, select that and click ok.<br />
Click ok to register this new PHP version.
</p>

<p>
  Close and relaunch ISS as admin. </br>
  Restart the server by clicking the icon at the top right.

<p>
<img src="https://i.imgur.com/zZINpnQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p> 

</p>

<p>
  From the Prerequisite files open the osTicket-v1.15.8.zip file. </br>
  Extract and copy the upload folder to your folder c:\inetpub\wwwroot</br>
  Rename the folder you just put in wwwroot to osTicket. </br>
  Close IIS, relaunch again as admin, and restart the server.</br>
  
</p>

<p>
 In the left column open the folders untill you reach osTicket folder.</br>
<p>
<img src="https://i.imgur.com/AcrYpEY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Double-click PHP Manager and click Enable or disable an extention.</br>
  From here you need to locate 3 extentions, "php_imap.dll, php_intl.dll, and php_opcache.dll.</br>
  Right click them and click enable.</br>
</p>
 
<p>
<img src="https://i.imgur.com/gGonUmW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
  Now you need to rename a file, go to C:\inetpub\wwwroot\osTicket\include and rename the file ost-sampleconfig.php to ost-config.php
</p>

<p>
  Right-click ost-config.php and go to properties. </b>
Go to security tab and click advanced. </b>
Click "Disable inheritance" then Click on "Remove all inherited permissions from this object"
</p>

<p>
 Click on add and then click "Select a principal" </b>
 In the little text box type "everyone" and click the "check names" buttion.</b>
 Click ok.</b>
 Check the "full Control" box and click OK</b>
 Click Apply and OK
</p>

<p>
From the Prerequisite files, Install Heidi SQL. (Filename example: HeidiSQL_12.3.0.6589_Setup.exe)</b>
You do not need to change any settings here, just install the default settings.</b>
Make sure the "Launch HeidiSQLL box is checks and finish the install.
</p>

<p>
For this tutorial we wont be updating HeidiSQL so skip the self update. </b>
At the bottom left click on "New"</b>
Fill out the root password you made earlier and click open.
</p>

<p>
  Now Right-click on "Unnamed-1", select create new, and then database.
  Under "Name" write "osTicket" then click ok.
</p>

<p>
Go to your web browser and go to http://localhost/osTicket/setup/</b>
Click Continue.</b> 
</p>
<p>
 Fill out your Help Desk's relavant information.</b>
 Under "database Settings" your "mySQL Database" is "osTicket", "MySQL Username" is "root", and your password will be your root password you set earlier.</b>
 Click Install Now.
 </p>

<p>
  Thats it for the installation of osTicket v1.15.8 
</p>

<p>
<img src="https://i.imgur.com/46MopJR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
