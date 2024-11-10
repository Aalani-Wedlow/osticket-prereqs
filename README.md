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

- IIS
- PHP Manager 
- Rewrite Module 
- VC_redist.x86.exe
- MySQL 5.5.62

<h2>Installation Steps</h2>

<p>
  <h3>1. Create a Virtual Machine</h3>
<img src="https://github.com/user-attachments/assets/08fe9792-5289-4d05-961a-1e0c0c3f373b" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Within Azure, select Windows 10 Pro under the "Image" to determine the operating system that your work will be displayed on. Be sure to choose a size of 2 vcpu's to ensure the virtual machine will run efficently. 
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/79ed836a-6b42-4d62-9be8-e50dd1ea8da6" height="80%" width="80%" alt="Disk Sanitization Steps"/>

  
  
  <h6>Note: the select imbound port, MUST be set to allow RDP (3389) to ensure Remote Desktop access to the virtual machine.<h6/>
</p>
<p>
  
</p>
<br />

<p>
  <h3>2. Identify your Virtual Machines IP adress</h3>
<img src="https://github.com/user-attachments/assets/3d24a1b3-6556-4735-9626-59630d2b6bad" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once the VM has been reviewed and created, the next step is to obtain it's public IP address. This will allow for the connection to the Remote Desktop program. 
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/4027d916-6d24-4cb6-9980-b1fb2a5d2b2b" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p> <h3>3.Enabling IIS</h3>
<img src="https://github.com/user-attachments/assets/b02fba25-1a99-4a8b-ae3c-5d1e76fed28e" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After the VM has been opened, IIS must be enabled. To test the connection to IIS, type 127.0.0.1 into the browser. In this case, the picture above shows a lack of a connection. 
</p>
<br />

<p> 
<img src="https://github.com/user-attachments/assets/c53e7d21-5dfe-4100-9864-dc58f746a698" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To enable IIS, go to the Control Panel. Under Programs and Features there will be an option to "Turn Windows Features on or off". After selecting that option, enable the features listed down below.
</p>
<br />

<p> 
<img src="https://github.com/user-attachments/assets/1e548a57-6f84-42e3-b3cb-bed9185698bc" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p> 
<img src="https://github.com/user-attachments/assets/257c5eb3-4018-45ee-ac40-da25509af52a" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Finally, test the connection once again by searching 127.0.0.1 into the browser. It should display the image above. 
</p>
<br />

<p> <h3>4. Install PHP</h3>
<img src="https://github.com/user-attachments/assets/d3a88bcd-86a8-4207-9fbc-07be90473d61" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Access the installation files install "PHPManagerForIIS_V1.5.0.msi"
</p>
<br />

<p> <h3>5. Install Rewrite Module</h3>
<img src="https://github.com/user-attachments/assets/7ae45888-2715-40d3-a8ce-a6e04ea2027a" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the installation files download "rewrite_amd64_en-US.msi"
</p>
<br />

<p> <h3>6. Create a new directory</h3>
<img src="https://github.com/user-attachments/assets/583d1c65-bd98-46ec-854a-bfb75e1e4bb4" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Within File Explorer, go under the C drive and create a file named PHP
</p>
<br />

<p> 
<img src="https://github.com/user-attachments/assets/b6e8fdeb-4b73-4877-b24d-74cfb1600566" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Extract the PHP zip file within the installation files into the new PHP folder.
</p>
<br />

<p> <h3>7. Install VC_redist.x86.exe</h3>
<img src="https://github.com/user-attachments/assets/c70a4cc6-eaaf-4a1e-bde8-989c3e95e928" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p> <h3>8. Install MySQL</h3>
<img src="https://github.com/user-attachments/assets/95c612ba-9740-4aed-a211-5a665dc5e48f" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h4>*When installing choose: Typical Setup--> Launch Configuration Wizard after install--> Standard Configuration</h4>
</p>
<br />

<p> <h3>9. Register PHP Manager</h3>
<img src="https://github.com/user-attachments/assets/afce7c80-85bc-46cf-8972-e03a721a20bd" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open IIS as an Administrator and selected "Register new PHP version". Place php-cgi.exe within the PHP file under the C drvie. 
</p>
<br />

<p> <h3>10. Restart IIS Server</h3>
<img src="https://github.com/user-attachments/assets/9ee7a553-1907-43f3-9f00-737baef4d171" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After completing the previous step, restart the web sever by right clicking your connection and pressing stop. Wait a few seconds and start it again.
</p>
<br />


<p> <h3>11. Downloading osTicket</h3>
<img src="https://github.com/user-attachments/assets/8d06c37e-5747-4ed4-8ca1-6164b289a764" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Extract osticket file and copy upload folder into inetpub folder under wwwroot (c:/inetpub/wwwroot). Then, rename "uplaod" file to "osTicket".
</p>
<br />

<p> <h3>12. Reload IIS</h3>reload 
<img src="https://github.com/user-attachments/assets/f77d906f-9b38-4a39-835e-2d26ea1955b2" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p> <h3>13. Launch osTicket</h3> 
<img src="https://github.com/user-attachments/assets/6fd92380-fbb6-48a8-86cc-8248ff4a0dc9" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Sites-->default website -->osTicket-->browse
</p>
<br />

<p> This screen should be displayed after clicking browse
<img src="https://github.com/user-attachments/assets/e44590a8-9751-4009-bc35-d62cfdf9a5a5" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p> <h3>14. Enable PHP Extensions</h3> 
<img src="https://github.com/user-attachments/assets/4fc3bab9-98a1-4d7b-b77f-f60b0d8abd0b" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Within IIS, enable the higlighted features:
 
  
  
  - php_imap.dll


  
  - php_intl.dll


  - php_opcache.dll

Once enabled, refresh the browser and some extensions should appear as active.
</p>
<br />

<p>  
<img src="https://github.com/user-attachments/assets/16947e7e-94ab-4b33-8d60-301fbaed9c6c" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p> <h3>15. Reanme ost-config.php</h3>
<img src="https://github.com/user-attachments/assets/b1dd7ce3-8eed-4e3e-b211-461652a2cf5d" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Rename "ost-sampleconfig" under c:/inetpub/wwwroot/osTicket/include to "ost-config.php".
</p>
<br />

<p> <h3>16. Assign Permissions</h3>
<img src="https://github.com/user-attachments/assets/d5f9c88d-8902-4dd1-b70c-267f1bf6158d" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Remove all inherited permissions--> add everyone as a principal (not reccomend to do in real situations)--> check all boxes to ensure all permissions are given 
</p>
<br />

<p> 
<img src="https://github.com/user-attachments/assets/82d3d561-7773-4f4c-8696-04deead7fe8d" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p> <h3>17. osTicket Setup Cont.</h3>
<img src="https://github.com/user-attachments/assets/547d41a4-5d26-40f2-ab34-e536f0f23a16" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Fill in the first half of the page by creating an Admin User and creating a name for the helpdesk. 
</p>
<br />

<p> <h3>18. Install HeidiSQL</h3> 

</p>
<p>

</p>
<br />

<p> With HeidiSQL, create a new database named "osTicket". Use SQL server login in from early to open it. make a connection with database, use sql server login in to open it, create a new data base named osTicket


  
<img src="https://github.com/user-attachments/assets/984854e6-fa40-4ca3-9f14-a60ea13038ca" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From here complete the botton portion of the osTicket instillation and it's complete. 
</p>
<br />




