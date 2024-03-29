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

- Add Internet Information Services
- Add MySQL 5.5
- Add all simple versions of x86 PHP up to v7.3
- Install osTicket v1.15.8
- Reload IIS (open IIS, Stop and Start the server)
- Enable extensions in IIS
- Refresh the osTicket site in your browser and observe the changes
- Clean up files for optimal use

<h2>Installation Steps</h2>

Add Internet Information Services
<p>
<img src="https://i.imgur.com/zHQ3ykz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 1 Install or enable IIS by opening the control panel. IIS will enable a web server on your computer to run osTicket from the web. You can do this by typing "control panel" from your search bar within your taskbar at the bottom of your desktop.
</p>
<br />

<p>
<img src="https://i.imgur.com/q3gcFY4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to Programs and select uninstall program.
</p>
<br />

<p>
<img src="https://i.imgur.com/EK6kueJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once you on the uninstall or change a program screen. Select Turn Windows features on or off on the right.
</p>
<br />

<img src="https://i.imgur.com/GR02SGf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Select the Internet Information Services radio button in the dialog box and click Ok.

<img src="https://i.imgur.com/77d9lAc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once IIS has been installed, search the internet for Microsoft Web Platform Installer and download this extension. You will need it to install the remaining software needed to install osTicket.

Add MySQL 5.5

<img src="https://i.imgur.com/THXv7zF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Add all simple versions of x86 PHP up to v7.3

<img src="https://i.imgur.com/X7Fu35v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Search the web and install: "Web Platform Installer" & open "Web Platform Installer". In the dialog box, search Web Platform Installer to add "MySQL 5.5" & search to add all simple versions of (x86) PHP up until 7.3

<img src="https://i.imgur.com/gWpbvb3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a username and password when asked to finish installation.

<img src="https://i.imgur.com/HTBMgNO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Web installer will attempt to finish installing all of the prerequisites that are checked (some of the downloads will fail, just manually download C++ redistributable & PHP Manager via files found online). 
Continue to finish with installation.
Find and install PHP Manager version 7.3.8 & version 1.5.0.

<p>
<img src="https://i.imgur.com/Pkh9Y3s.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

  
Install Microsoft Visual C++
<p>
<img src="https://i.imgur.com/xcIWPE5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
Install PHP Manager

Install osTicket v1.15.8
<p>
<img src="https://i.imgur.com/eqFSUiY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Installation errors should be fixed at this point. Download and install the osTicket software. You will need to extract the zip file once downloaded.
<p>
<img src="https://i.imgur.com/UPXpiYv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Once osTicket has been installed, open the download folder and copy it into your wwwroot folder that was created from IIS and rename the folder from upload to osTicket. filepath ThisPC/Windows (C:)/inetpub/wwwroot
<p>
<img src="https://i.imgur.com/mzNsDKY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Rename the upload folder to osTicket in the wwwroot folder

Reload IIS (open IIS, Stop and Start the server)
<p>
<img src="https://i.imgur.com/oXT19Dq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Go to -->Taskbar-->Type IIS in the searchbar and open the program-->You will need to restart the web server by selecting the browse 80 folder in the connections folder. -->Sites-->osTicket-->browse80-->stop-->restart

<p>
<img src="https://i.imgur.com/5gIVfsA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
If the program was properly installed, you will see this prerequisite screen. If not, please go back and install the missing php, C++, or php manager. We will now enable eextensions.

Enable extensions in IIS

<p>
<img src="https://i.imgur.com/udxfNHH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Enable the following extensions, php_imap.dll, php_intl.dll, and php_opcache. Please refresh the osTicket site and observe the changes.

<p>
<img src="https://i.imgur.com/9Jyrbzi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to C:-->inetpub-->wwwroot-->osTicket-->include and right-click the ost-sampleconfig.php file and rename it to ost-config.php

<p>
<img src="https://i.imgur.com/uZR6cvY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Enable automatic permissions for everyone in this file by right-clicking on the file and select -->Properties-->Advanced-->Disable inheritance-->type everyone in the next dialog box-->selct the Full Access radio button-->Select the Apply button-->Select the Ok button

<p>
<img src="https://i.imgur.com/8fczdiw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install HeidiSQL for osTicket to have a client database that connects to MySQL that was installed previously.

<p>
<img src="https://i.imgur.com/EP3idvb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To create a database, you will need the username and password that was used to install MySQL. Create a new database by right-clicking on SSS-->New-->Database-->> name your database osTicket and click Ok.

<img src="https://i.imgur.com/KWNWOKb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to your osTicket installer in your browser tab and fill out the following information in the fields. --> System Settings-->Admin User-->Database Settings--> Click on "Install Now"

Refresh the osTicket site in your browser and observe the changes
<p>
<img src="https://i.imgur.com/8G89n6U.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
This screen will show a successful installation of osTicket

Clean up files for optimal use
<p>
<img src="https://i.imgur.com/KTZ9fhl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lastly, we will clean up some files during installation to prevent future performance issues with osTicket. Go to your C:-->inetpub-->wwwroog-->osTicket and delete the setup file

<p>
<img src="https://i.imgur.com/nacJmFL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to C:-->Inetpub-->wwwroot-->osTicket-->inlclude and right click on ost-config.php and select securities tab-->advanced-->click edit to change permissions for everyone to only have read & execute by deselecting the radio buttons. Click on apply-->Ok



