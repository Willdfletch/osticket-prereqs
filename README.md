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

- Computer
- Azure Subscription/Free Trial

<h2>Installation Steps</h2>

Set up the Virtual Machine in Microsoft Azure
- Create an Azure Virtual Machine Windows 10, 4vCPUs
  - Select an appropriate region
  - Select Windows 10 OS

![image](https://github.com/user-attachments/assets/06fea6c4-1b9c-4265-8f00-fd64867b69f3)

Confirm Liscencing, and click Review + Create

- Navigate to the Virtual Machine and find the public ip address
   - Open Remote Desktop and connect to the Virtual Machine
   - Launch Microsoft Edge within the VM
   - Download https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD within the VM (osTicket system)

  Open Control Panel, navigate to Programs and Features, and click "Turn Windows Features on or off"
  

  ![image](https://github.com/user-attachments/assets/b68c202a-5d02-44ff-ac4b-1fb32d4beba0)

Afterwards, you will want to enable Internet Information Services, and CGI (which is under ADF)
 - Click okay, and it will install the files

![image](https://github.com/user-attachments/assets/5f4ff795-db5f-4c05-9dfb-f31b7ce6b05f)

Now, navigate to the osTicket Installation files, right click and unzip it onto the VM Desktop
- Once done, download PHP Manager and the Rewrite module

![image](https://github.com/user-attachments/assets/64685399-5fe9-41fe-a5c0-175c9a733971)

Create a new folder "PHP" on the VM's C Drive
- From the osTicket folder, extract the php 7.3.8 folder into the "C:\PHP" folder
- From the osTicket folder, install VC_redist.x86.exe
- From the osTicket folder, install MySQL.5.5.62, and choose "Typical" setup
    - You will choose "Standard" configuration and set up your security settings, and click "Execute" 


![image](https://github.com/user-attachments/assets/f9fed873-8cf4-4df4-a866-fc78ff64a1b8)

Open IIS as an Admin

Register PHP from within IIS
- Reload IIS (Open IIS, Stop and Start the server)

  
![image](https://github.com/user-attachments/assets/a9bba10f-c799-4013-8545-a6c6825df551)

Navigate to the osTicket installation files, extract “osTicket-v1.15.8.zip” and copy the upload folder into “c:\inetpub\wwwroot” (root is what I named my server, yours might be something different)
 - Rename "Upload" to "osTicket"
 - Reload IIS (Internet Information Services, Stop and Start the server)

![image](https://github.com/user-attachments/assets/812a7a38-3b65-4c22-85f4-5042c9579ada)

Go to sites -> Default -> osTicket
 - Click “Browse *:80” on the right
   
![image](https://github.com/user-attachments/assets/2ca5f889-33a7-44a3-8bde-5a4630cf0e41)

Navigate to sites -> "Default Web Site" -> "osTicket"
- Double click PHP Manager
- Click "Enable or disable an extension"

   - Enable: php_imap.dll

   - Enable: php_intl.dll

    - Enable: php_opcache.dll

At the end it should look like this!

![image](https://github.com/user-attachments/assets/409be26d-a088-43db-9b5f-af47f7413849)

Refresh the osTicket site in your browser

Navigate to ost-sampleconfig.php and rename it to ost-config.php

![image](https://github.com/user-attachments/assets/736cc472-0062-4e3f-b260-f63b06a739ff)

Assign Permissions to "ost-config.php"
  - Assign permissions acoordingly in a secure manner, or if you're just testing click "Disable inheirtence" ---> Add ---> Select principle -> Everyone -> All

Navigate back to the osTicket in the browser, and fill out the following page
- Name your helpdesk
- Default email (receieves emails from customers)

From the "osTicket-Installation-Files" folder, install and launch HeidiSQL

![image](https://github.com/user-attachments/assets/bc69f789-9563-44c5-a60f-45667a2f68c5)


![image](https://github.com/user-attachments/assets/ed524aa6-d9a3-47c5-bc84-ab55c029c5e4)

Continue setting up osTicket in the browser
 - Connect SQL Server to your Database within HeidiSQL
 - Fill out "MySql Database", "MySQL Username", "MySQL Password" in the osTicket browser
 - Click "Install Now!"





<h1>It should now be setup, and ready to go!</h1>



