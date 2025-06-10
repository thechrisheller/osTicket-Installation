
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 (22H2)</b> 

<h2>List of Prerequisites</h2>

osTicket Files

- All Items: [osTicket Installation Files](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD)

<h2>Installation Steps</h2>

<p>

<h2>STEP 1 - Create a Virtual Machine - I will be using Microsoft Azure</h2>

Once you create your VM on Azure, copy the public IP Address that is populated for you when creating the Windows VM. (Example: the public IP that was populated for me was 20.51.217.72) Use Remote Desktop and sign in using the login credentials you have chosen.

![osTicketLab-Step-1](https://github.com/user-attachments/assets/571b9d0e-624c-4f04-a077-d99f7370716a)

<h2>STEP 2</h2>

- Download the [osTicket Installation Files](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD) inside your Virtual Machine. Once they download, go ahead and extract the files. I extracted them to the desktop for easy access.

![osTicketLab-Step-2](https://github.com/user-attachments/assets/41173e90-15d6-498a-b17e-82bbd1044029)

<h2>STEP 3 - Install | Enable IIS in Windows WITH CGI</h2>

- Go to "Control Panel" > Under Programs ”Uninstall Program” > "Turn Windows features on or off"

![osTicketLab-Step-3a](https://github.com/user-attachments/assets/951a3122-d0cb-4b35-a689-ccc24dbf6df5)

- Check the "Internet Information Services" box > Expand the box

![osTicketLab-Step-3b](https://github.com/user-attachments/assets/50487ff3-2cde-450d-b6a7-1c5cd694414b)

- Expand "World Wide Web Services" > Expand "Application Development Features" > then Check the "CGI"

![osTicketLab-Step-3c](https://github.com/user-attachments/assets/2e81a392-881d-4833-8ac9-ba8f626407a3)

<h2>STEP 4 - Install: PHP Manager | Install: rewrite_amd64_en-US.msi File</h2>

Go back to the osTicket Installation Files we extracted back in step 1 and open the folder, and Download
 - PHPManagerForIIS_V1.5.0
 - rewrite_amd64_en-US

![osTicketLab-Step-4](https://github.com/user-attachments/assets/f60702a4-24c6-4e36-9bf8-55cfc9f7f6a5)

<h2>STEP 5</h2>
 
 - Create a Folder in "Windows (C:) called "PHP" | unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder

![osTicketLab-Step-5](https://github.com/user-attachments/assets/14223602-c74c-4da4-92a8-379d3913713a)

 - Extract PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder

 - Go back to the osTicket Installation Files that we extracted from step 1 and right click, and extract all of "php-7.3.8-nts-Win32-VC15-x86" file and extract it to the "PHP" folder we just created.

![osTicketLab-Step-5b](https://github.com/user-attachments/assets/512c88d9-cbbf-4c44-b5bc-ed68d68dd996)


<h2>STEP 6</h2>
 
 - Install "VC_redist.x86"

![osTicketLab-Step-6](https://github.com/user-attachments/assets/3ca2a0f3-3395-44a5-b14f-ebbcf39fa4e0)

<h2>STEP 7</h2>

 - Install "MySQL 5.5.62"
 - Install "MySQL 5.5.62"

![osTicketLab-Step-7a](https://github.com/user-attachments/assets/611296bc-41fa-4b9a-9cc9-6478783bfa9b)

 - Typical

![osTicketLab-Step-7b](https://github.com/user-attachments/assets/c3e0421e-337e-4486-8f73-052b4ea3c959)

 - Couple of "next"

![osTicketLab-Step-7c](https://github.com/user-attachments/assets/21e80ab6-6db5-4b1a-a1d7-c0ed52f9d68c)

 - Make sure you select "Standard Configuration"

![osTicketLab-Step-7d](https://github.com/user-attachments/assets/779b9ae0-0282-46d0-90b4-c944c38f364a)

 - Next

![osTicketLab-Step-7e](https://github.com/user-attachments/assets/be8379fb-3297-4331-8908-1634558a5b9a)

 - Create your root username and password, and DO NOT FORGET IT!

![osTicketLab-Step-7f](https://github.com/user-attachments/assets/ce30009b-fbd8-4cd5-bdfe-e11e6e3dbed0)

 - Execute and complete

![osTicketLab-Step-7g](https://github.com/user-attachments/assets/1da6d30c-cd07-4378-839b-51e75ba99b78)

<h2>STEP 8 - Open IIS as an Admin</h2>

![osTicketLab-Step-8a](https://github.com/user-attachments/assets/ef45eb20-3b41-437b-aa7e-7754ecae14e5)

 - This is what IIS should look like

![osTicketLab-Step-8b](https://github.com/user-attachments/assets/c3be8b1d-d9ba-47e7-b683-815e0281310e)

<h2>STEP 9 - Register PHP from within IIS | Reload IIS</h2>

 - Click PHP Manager

![osTicketLab-Step-9a](https://github.com/user-attachments/assets/711b3bb5-aeaa-4554-9696-20a415c06739)

 - Select "Register new PHP version"

![osTicketLab-Step-9b](https://github.com/user-attachments/assets/9831b282-482a-430b-9226-b0139a90d904)

 - Select the "..."

![osTicketLab-Step-9c](https://github.com/user-attachments/assets/8d6dbfa7-9a4b-4cf1-a97d-cae76cd6db34)

 - This PC > Window (C:) > PHP Folder > Select "php-cgi" (Application)

![osTicketLab-Step-9d](https://github.com/user-attachments/assets/c2ba86dc-fac7-4ea7-be9e-a6ff8a3f3242)

 - Go back to the original screen and select "stop" then select "start" on the top right

![osTicketLab-Step-9e](https://github.com/user-attachments/assets/05387786-a128-4bbd-b781-a668107f9d5d)

<h2>STEP 10 - Install osTicket</h2>

 - Select osTicket Installation File > Right Click and Extract all "osTicket-v1.15.8"

![osTicketLab-Step-10a](https://github.com/user-attachments/assets/8d61f349-105d-4c35-bc5e-bfe5c8ffa166)

 - Open a second file explorer folder and select This PC > Windows (C:) > inetpub > wwwroot

![osTicketLab-Step-10c](https://github.com/user-attachments/assets/f0a8e8b1-8a92-458c-9a56-4af526987813)

 - In the osTicket Installation file, we just extracted "osTicket-v1.15.8"

Find the upload file and move it to the wwwroot folder

![osTicketLab-Step-10d](https://github.com/user-attachments/assets/fd7c2353-197f-4162-bb38-848d71ee63fc)

 - Rename the upload file to "osTicket" and make sure it is spelled correctly

![osTicketLab-Step-10e](https://github.com/user-attachments/assets/816b074e-f49d-429c-8bc1-abf0e9c05280)

<h2>STEP 11 - Reload IIS</h2>

 - Once you get loaded back into IIS as Admin > select "stop" and then "start" like we did in step 9
 - From there toggle down "Sites" > "Default Web Site" > Select "osTicket

![osTicketLab-Step-11a](https://github.com/user-attachments/assets/c8aaf948-9eba-44d7-920f-350d44fd7805)

 - Select "Browse *:80 (http)"
 - Once you select that, osTicket should load onto your web browser

![osTicketLab-Step-11b](https://github.com/user-attachments/assets/6294d6de-6e43-43ac-b57c-62f7bca65f92)

 - Remember all the X's from this page for the next step and once we complete the next step notice a change in them

<h2>STEP 12 - Enabling Some Extensions</h2>

 - IIS as Admin > Site > Default Web Site > osTicket > PHP Manager

![osTicketLab-Step-12a](https://github.com/user-attachments/assets/e1f937a8-fbf0-4255-946a-6b5a3cda396f)

 - PHP Extensions > Enable or disable an extension

![osTicketLab-Step-12b](https://github.com/user-attachments/assets/fa5bbf5c-3baf-40fe-8ce8-80c0a9d8761a)

 - Enable php_imap.dll | Enable php_intl.dll | Enable php_opcache.dll

![osTicketLab-Step-12c](https://github.com/user-attachments/assets/cb9631c2-c34a-45e1-b5e3-86b2cd554222)

 - Back to the Web Browser and refresh the page, and notice that you have more extensions 

![osTicketLab-Step-12d](https://github.com/user-attachments/assets/2c6dde31-67aa-433b-bc46-e4327bb07878)

<h2>STEP 13</h2>

 - Rename: ost-config.php
 - This PC > Windows (C:) > inetpub > wwwroot > osTicket > Include
 - Scroll down to where it says ost-sampleconfig.php

![osTicketLab-Step-13a](https://github.com/user-attachments/assets/23f9644c-a4fa-4694-9789-eb06dc86c85a)

 - Rename it to ost-config.php

![osTicketLab-Step-13b](https://github.com/user-attachments/assets/eb0171f7-b435-461e-ab1f-fa888de7f1e8)

<h2>STEP 14</h2>

- Assign Permissions: ost-config.php
- Right click ost-config > Properties

![osTicketLab-Step-14a](https://github.com/user-attachments/assets/7cc1c05b-590e-4f72-8985-957ac127605e)

 - Security > Advanced

![osTicketLab-Step-14b](https://github.com/user-attachments/assets/04484f60-fcaa-4646-898c-37be3c4a4da7)

 - Disable Inheritance
 - Remove all

![osTicketLab-Step-14c](https://github.com/user-attachments/assets/382c0014-88b9-4cbc-93ce-dd244a21bb71)

 - Add

![osTicketLab-Step-14d](https://github.com/user-attachments/assets/80775e0b-85d1-4830-9836-abed88a38211)

 - Select a principal

![osTicketLab-Step-14e](https://github.com/user-attachments/assets/d3e95b26-e3bd-4262-a03f-1507f7a039d0)

 - Type Everyone > select Check Names > you should see Everyone be underlined > then select OK
 - This isn't good in real life, but for lab and practice purposes, this is fine.

![osTicketLab-Step-14f](https://github.com/user-attachments/assets/02da36c8-a16a-48fe-acfe-636509481e7b)

 - Select Full Control > Select OK

![osTicketLab-Step-14g](https://github.com/user-attachments/assets/0d18d19d-926c-4e82-a642-193722e0f94c)

 - Select Apply > Select OK

![osTicketLab-Step-14h](https://github.com/user-attachments/assets/24a76d66-7811-4325-bdf8-534e1c8d16a1)

<h2>STEP 15 - Setting osTicket in the web browser</h2>

 - Select Continue in the Web Browser for osTicket

![osTicketLab-Step-15a](https://github.com/user-attachments/assets/d8cde6c3-5988-4bbd-9827-029a69b1324c)

 - Fill out the basic information and make sure that you remember the username and password, and make sure the email addresses are different.

![osTicketLab-Step-15b](https://github.com/user-attachments/assets/1942e4af-f0e4-4e4c-b766-e7cd208ebc8a)

 - Back to osTicket Installation Files folder > Install HeidiSQL_12.3.0.6589_Setup

![osTicketLab-Step-15c](https://github.com/user-attachments/assets/c01d8078-6888-4853-9a95-37a17d0541d6)

 - Once installed > select New

![osTicketLab-Step-15d](https://github.com/user-attachments/assets/7d9391ae-a18b-49bf-9e89-cd0891b774cb)

 - Back in step 7, enter the password you selected and select Open.

![osTicketLab-Step-15e](https://github.com/user-attachments/assets/3fa80357-02fb-4998-afe0-0d63b8a47194)

 - Right Click Unnamed > Create new > Database

![osTicketLab-Step-15f](https://github.com/user-attachments/assets/2a89b9a4-7d88-4f48-8319-83249a63dac5)

 - Type in osTicket and make sure it is spelled exactly like that > select OK

![osTicketLab-Step-15g](https://github.com/user-attachments/assets/691f3b53-070b-4525-9a67-1f07e815e9c9)

 - Back to the web browser and enter your credentials you selected and then select "Install Now"

![osTicketLab-Step-15h](https://github.com/user-attachments/assets/7256672b-47ed-4543-b8a9-c5346a901b2e)

 - Congrats, you have installed osTicket!!!

![osTicketLab-Step-15i](https://github.com/user-attachments/assets/f4ae92b2-ce20-4fec-a965-def5f75606c7)

<h2>Final Step - Check to see if you can log in as admin</h2>

- Copy Paste Into VM Browser
- [http://localhost/osTicket/scp/login.php](http://localhost/osTicket/scp/login.php)

![Final Step 1a](https://github.com/user-attachments/assets/e20fbde8-600b-4a8e-81ce-7e80389e8176)

 - Once Logged in this is what the dashboard should look like.

![Final Step 1b](https://github.com/user-attachments/assets/1ba5f5ec-7b90-4230-9e20-34c9b5cfa5ed)

<h2>Conclusion</h2>

This concludes our project. We successfully installed osTicket on our Windows virtual machine! Make sure to stop the VM in Azure so that you don't run up your bill while not in use. 
