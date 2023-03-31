<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket. osTickicket allows users to create and manage associates access to tickets as well as allow the creation of tickets by those employees or users / customers. This is part 1 of 4 that will go over installing, setting up and using osTicket and its commonly used features. We will be installing osTickoet on Microsoft Azure a cloud service where we can creat and host the virtual machines needed for this lab.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)
<h2>Outline of steps in part one</h2>
In part one we will 

- Create a rescource group
- Set up our virtual machines in the Azure rescource group  
- RDP (remote desktop protocol) into the VM
- Enable IIS (Internet Information Services)
- Install osTicket on the VM
- Clean up of unnecessary files (After this you can move on to <a href="https://github.com/TimjMerida/osTicket-pt2-Post-Installation-Configuration">part 2</a>)

<h2>Installation Steps</h2>

<p>
<img src="https://user-images.githubusercontent.com/128980344/228999887-c8db8e47-5c22-4b6e-bf59-6fdbc04e66cd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Before starting I recommend opening a notepad to keep important information. You could also write it down or use an app. 
  
The first thing we need to do is create a rescource group for our VM's. On the Azure homepage you can either click on rescource groups or search for it at the top. Once it is open click create at the bottom. I will have all my rescources I create be in the same region and I reccomend you do as well. I will be using US east as the region. If you are using other regions know that some rescources may not be available or will have price differences on Azure. 
  
You can name the rescource group what you like I will be calling mine osTicket-RG (Write your rescource group namne and region down). We do not need any tags so click review and create at the bottom. Once its validated click create and we have our rescource group.
  
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/229000988-75956759-edfc-4af7-aff3-d938866f8bb3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

</p>



Next we need to make the VM's for this lab. Go back to the homepage and click Virtual machines or type in the search bar and look up virtual machines. Click create and select Azure Virtual Machines. This is where we will put in our setting for our virtual machine. First under rescource group select the one we have created for this lab. Next name the machine, I will be naming it VM-1-osTicket-Lab. Next select the image type, we will be using windows 10 in this lab. After change the region to the same region your rescource group was created. For availibility options select no infastructure redundancy required.  




<br />
<p>
  
  
<img src="https://user-images.githubusercontent.com/128980344/229002483-0fc2e9ab-62c7-4514-bec3-60f02b2232d4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>

  
  
  
  
*Your options may depend on the selected region*
Scroll down and select the size, I reccomend at least 2 vcpus or the VM will be slow. Next type in a username and password. Write them down as we will need them later. I will be using oslabuser for the username and Password12321 for the password. At the very bottom select the checkbox for liscensing. 
  
  
  
  
</p>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Scroll back to the top and select networking. 
</p>
<br />


























