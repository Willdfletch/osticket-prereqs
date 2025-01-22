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





<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
