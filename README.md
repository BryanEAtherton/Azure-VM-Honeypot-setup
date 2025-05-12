# Security-Project-1

<p align="center">
<img src="https://i.imgur.com/NNk2ICv.jpg"/>
</p>

<h1>Azure Virtual Machine Honeypot Setup</h1>
Here we will set up 2 Azure Virtual Machines, 1 Windows and 1 Linux, to use in our Security Project as honeypots. We will disable the firewall protections at the Azure level to open the machines to the internet.

<h2>Environments and Technologies Used</h2>

- Microsoft Azure
- Azure Network Security Groups (NSG)


<h2></h2>
 

<h2>Virtulal Machine Setup in Azure </h2>




</p>
<br />
1.  In Azure Create 2 VMs - 1 Windows & 1 Linux.
<p>
<img src="https://i.imgur.com/QSn0enR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
[Click here to view instructions on how to create and access an Azure VM using Remote Desktop](https://github.com/BryanEAtherton/Azure-Virtual-Machine)
</p>
<br />

 <p>
2. Navigate to the Linux VM NSG and disable the Firewall by deleting the SSH inbound rule. 
<p>
<img src="https://i.imgur.com/CCWUnuQ.png" height="50%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/E7EQyPj.png" height="50%" width="40%" alt="Disk Sanitization Steps"/>
</p>

<p>
 3. Create a new rule to allow all traffic into the VM.
<p>
<img src="https://i.imgur.com/3NPTV98.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/8iTnSg6.png" height="50%" width="40%" alt="Disk Sanitization Steps"/>
 <p>
   
4. Repeat the same process for the Windows VM by deleting the RDP inbound rule.

<p>
<img src="https://i.imgur.com/vYFfEl4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>
<p>
5. Repeat step 3 for the Windows VM and create a new rule to allow all traffic into the VM.
<p>
<img src="https://i.imgur.com/EoHjiaZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p>
  
[Click here to view instructions on how to create and access an Azure VM using Remote Desktop](https://github.com/BryanEAtherton/Azure-Virtual-Machine)
</p>
<br />




