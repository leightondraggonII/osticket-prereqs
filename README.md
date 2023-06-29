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
   
   Let Azure validate your VM and click create after. If your VM is not validated, it means that there was error in your selections or (in my personal experience) a error in the validation process on Azure's end. In that case just retry validating it with the same selections again. Click create after the validation is passed.
   
  <p>
   
   <img src="https://i.imgur.com/bDVzufU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
   
   Azure will begin deloying your VM. After the deployment process is done, you can click "Go to resources" to immediately access your VM's overview page, or you can navigate to it through "Virtual Machines" page.
   
   
   
  

<br />

<p>
<img src="https://i.imgur.com/shd9TVn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/shd9TVn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>
<p>
On the VM overview page, copy the public IP address.
</p>
<br />

<p>
<img src="https://i.imgur.com/3n97cE6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/iyn8p1S.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On your desktop, search "remote desktop connection" and click on the application. On the logon settings, paste the copied public IP address from the VM overview page and enter your chosen username from the VM creation process.
</p>
<br />

<p>
<img src="https://i.imgur.com/9cNoeSY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/jl7KyV1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/RWsOQXq.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 After clicking connect, another window will ask you to confirm your credentials to connect to the VM. A security window will appear after saying the "remote computer cannot be verfied", just click yes to connect to the VM. A window should appear with familiar Windows login screen, you are connected to the virtual machine.

</p>
<br />

<p>
<img src="https://i.imgur.com/ItMgiY5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/NMGF1qG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 After you logon to your VM, open up Microsoft Edge and download the installation files from this link "https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6". The zip file should be located in the VM downloads folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/2d7Vsmo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/eJ3CAnE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/K80Jtvt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we need to enable Windows Internet Information Services (IIS) with Common Gateway Interface (CGI). Open up Control Panel either by using the searchbar or Run "control" command. Click on Programs and then "Turn Windows features on or off".
</p>
<br />

<p>
<img src="https://i.imgur.com/ciEfQMx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/WK0jJp5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Expand the Internet Information Services tab by clicking the box symbol next to it. Do the with "World Wide Web Services" and then "Application Development Features". Check the box that says "CGI" and click ok.
</p>
<br />

<p>
<img src="https://i.imgur.com/antVLUG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/In7gSwj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Navigate back over to your Installation Files folder and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi). Just continue through the installation with standard settings unchanged.

</p>
<br />

<p>
<img src="https://i.imgur.com/AzvbtOS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Fl6OGVJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After installing PHP Manager, again navigate to back to the installation folder and install the Rewrite Module (rewrite_amd64_en-US.msi). All defualt settings like the last step.
</p>
<br />

<p>
<img src="https://i.imgur.com/PhYqTfM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/3BFUiZp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/dSuuROH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Create a folder named "PHP" in your C: drive directory. In your Installtion Files folder there is a zip file named "php-7.3.8-nts-Win32-VC15-x86.zip", exact the contents on that file into the PHP folder we just made.


</p>
<br />

<p>
<img src="https://i.imgur.com/pDnZDM6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/x6sZdyE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Returning again to the Installation Files folder install VC_redist.x86.exe. Defualt settings the same as before.
</p>
<br />

<p>
<img src="https://i.imgur.com/sDADVgZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/gVmExPq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/DmA9JTU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After that, begin the install of MySQL 5.5.62 as well.
</p>
Select "Typical install"
</p>
Leave "Launch Configuration Wizard" check after and click "Finish"
</p>
Check "Standard Configuration" on the second window
</p>
Create a Root Password for your service
</p>
<br />

<p>
<img src="https://i.imgur.com/uFwSTaq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/ywKwvUA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/dhAFBDV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/F3Nh665.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/v4w3ew1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/KuaMzFR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open the IIS program as a adminstrator by right-clicking and selecting the option.
<p>
PHP Manager should appear after opening as admin, open PHP Manager.
 <p>
Click "Register new PHP Version".
  <p>
Locate "php-cgi.exe" in the PHP folder we made earlier, through the applications file search.
 <p>
 Highlight the "OSticket-VM (OSticket-VM\your username).
  <p>
  Click "restart" in the Action tab to the right.

</p>
<br />

<p>
<img src="https://i.imgur.com/jfnXHQw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/nYoMI7Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Returning to the Installion Files folder, extract the "upload" folder and copy it to the path c:\inepub\wwwroot.
<p>
Rename upload folder to "osTicket".
<p>
Restart the IIS program like in the previous step.
</p>
<br />

<p>
<img src="https://i.imgur.com/Nw2i85L.png="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/430SZJu.png="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/GLHvttp.png" height="80%" width="80%" alt="Disk Sanitization Steps>
 <p>
On the IIS program click “Browse *:80”.
 <p>
Navigate to Sites\default\osTicket in IIS
  <p>
 Open up PHP Manager
 <p>
 Click "enable or disable an extension"
 
<br />

<p>
<img src="https://i.imgur.com/3n97cE6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/3n97cE6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

























