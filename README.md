<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Virtual Machine Setup</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket. osTickicket allows users to create and manage associates access to tickets as well as allow the creation of tickets by those employees or users / customers. This is part 1 of 4 that will go over installing, setting up and using osTicket and its commonly used features. We will be installing osTickoet on Microsoft Azure a cloud service where we can creat and host the virtual machines needed for this lab.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- RDP (Remote Desktop Protocol)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)
<h2>Outline of steps in part one</h2>
In part one we will 

- Create a rescource group
- Set up our virtual machine in the Azure rescource group 
- Connect to the VM with RDP

<h2>Virtual Machine Setup</h2>

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
<img src="https://user-images.githubusercontent.com/128980344/229003230-b4a19e3e-d935-4272-8d3c-d0afbb04cb8c.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Scroll back to the top and select networking. We will have azure create a virtual network for us. The setting should be simmilair to mine. Afterwards select review and create at the bottom and allow it to validate. Once validated we can create the VM! It may take some time to create once created it should say your deployemnt is complete. You can go back to the azure homescreen or click on go to rescource and you are ready for the next <a href="https://github.com/TimjMerida/osTicket-pt2-Post-Installation-Configuration">part</a>!  
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/229168973-7bd8f8eb-f3aa-40dc-8971-538e445ff549.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Before we can start downloading osTicket we need to RDP (Remote Desktop Protocol) into the VM. Start by going to VM's in Azure and going to virtual machines. Select the VM you are using for this lab (VM-1-osTicket-Lab if you are following along). We need the public ip adress on the right.
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/229169860-e059a965-30c5-4c34-a48e-1abdfe6d1f4b.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
On your windows desktop click the windows icon and search RDP. Open remote desktop and type in your VM's public IP adress, then click connect.  
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/229403077-096a5d2d-8261-45b8-b837-2fbe38f25d44.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://user-images.githubusercontent.com/128980344/229403360-e7233172-a419-46e3-8378-d66fb7bc2883.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
We have to sign in with the username and password we created in part <a href="https://github.com/TimjMerida/osTicket-pt1-VM-setup">one</a>. To do this click more choices and enter the credentials you created. The username and password I set were oslabuser and Password12321. After clicking ok there will be a popup. Click yes to connect to the VM.
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/229172217-f634a6d5-2066-4b17-a564-90ace922c995.png"  height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>

<p>
After conecting you will get to choose privacy settings. You can turn all these off for this lab.
</p>
<br />











