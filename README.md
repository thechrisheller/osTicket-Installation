
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

STEP 1 - Create a Virtual Machine - I will be using Microsoft Azure

Once you create your VM on Azure, copy the public IP Address that is populated for you when creating the Windows VM. (Example: the public IP that was populated for me was 20.51.217.72) Use Remote Desktop and sign in using the login credentials you have chosen.

![osTicketLab-Step-1](https://github.com/user-attachments/assets/571b9d0e-624c-4f04-a077-d99f7370716a)

STEP 2 - Download the [osTicket Installation Files](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD) inside of your Virtual Machine. Once they download, go ahead and extract the files. I extracted them to the desktop for easy access.

![osTicketLab-Step-2](https://github.com/user-attachments/assets/41173e90-15d6-498a-b17e-82bbd1044029)

STEP 3 - Install | Enable IIS in Windows WITH CGI

- Go to "Control Panel" > Under Programs ”Uninstall Program” > "Turn Windows features on or off"

![osTicketLab-Step-3a](https://github.com/user-attachments/assets/951a3122-d0cb-4b35-a689-ccc24dbf6df5)

- Check the "Internet Information Services" box > Expand the box

![osTicketLab-Step-3b](https://github.com/user-attachments/assets/50487ff3-2cde-450d-b6a7-1c5cd694414b)

- Expand "World Wide Web Services" > Expand "Application Development Features" > then Check the "CGI"

![osTicketLab-Step-3c](https://github.com/user-attachments/assets/2e81a392-881d-4833-8ac9-ba8f626407a3)

STEP 4 - Install: PHP Manager | Install: rewrite_amd64_en-US.msi File

Go back to the osTicket Installation Files we extracted back in step 1 and open the folder, and Download
 - PHPManagerForIIS_V1.5.0
 - rewrite_amd64_en-US

![osTicketLab-Step-4](https://github.com/user-attachments/assets/f60702a4-24c6-4e36-9bf8-55cfc9f7f6a5)

STEP 5 - Create a Folder in "Windows (C:) called "PHP" | unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder

![osTicketLab-Step-5](https://github.com/user-attachments/assets/14223602-c74c-4da4-92a8-379d3913713a)

 - Extract PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder

Go back to the osTicket Installation Files that we extracted from step 1 and right click, and extract all of "php-7.3.8-nts-Win32-VC15-x86" file and extract it to the "PHP" folder we just created.

![osTicketLab-Step-5b](https://github.com/user-attachments/assets/512c88d9-cbbf-4c44-b5bc-ed68d68dd996)


STEP 6 - Install "VC_redist.x86"

![osTicketLab-Step-6](https://github.com/user-attachments/assets/3ca2a0f3-3395-44a5-b14f-ebbcf39fa4e0)

STEP 7 - Install "MySQL 5.5.62"

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




