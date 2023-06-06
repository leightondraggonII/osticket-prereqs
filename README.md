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

- A Windows 10 Virtual Machine (VM) in Microsoft Azure
- Download the necesarry [Installation Files](https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)
- Enable / Install IIS in Windows with CGI
- Install the files from the [Installation Files](https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) Google Drive folder
- Finalize the installation of osTicket in the broswer

<h2>Installation Steps</h2>

<p>
Before making a VM, you must first create a Resource Group. This resource group is going to house the VM and whatever resources is needed for a specific solution on Azure.

<img src="https://i.imgur.com/xgurseo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p>
 
 Type "Resource Group" in the searchbar and click on the link with the same name. 
<img src="https://i.imgur.com/EueHUmp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <p>
  On that page click the create button.
<img src="https://i.imgur.com/kN0QrIT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/yVN5vOA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <p>
   Select your Subscription, name your Resource Group, select the region you want your Resource Group to be located and click "review & create".
   
   <p>
   
   <img src="https://i.imgur.com/26nN6tT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
   <p>
    Type "Virtual Machine" into the searchbar and click the tab of with the same name. On that page click the "create" button and select "Azure Virtual Machine" from it.

 Go to the [Microsoft Azure Portal](https://portal.azure.com/) after creating your first subcription to use the service. Type "Resource Groups" and click the link with the same name. Give Azure some time for it validate the creation of your Resource Group and click "Create" after.

</p>
 

<p>
Choose your subscription and resource group. Name your VM and select what region you want your VM to be in. Choose Windows 10 Pro, x64 as your image. Leave everything else on the screenshot as is.
</p>

<img src="https://i.imgur.com/of8FVrx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <p>
 Choose the size of your virtual machine (CPU cores and Memory). Create a user name and password for access to your VM. Click "Review and Create".
 <p>
  
  <img src="https://i.imgur.com/0vpu3A2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
  <p>
   
   Let Azure validate your VM and click create after. If your VM is not validated, it means that there was error in your selections or (in my personal experience) a error in the validation process on Azure's end. In that case just retry validating it with the same selections again.
   
  

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
