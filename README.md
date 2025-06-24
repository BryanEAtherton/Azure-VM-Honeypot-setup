# Honeynet and SOC in Azure

<p align="center">
<img src="https://i.imgur.com/NNk2ICv.jpg"/>
</p>

<h1>Azure Virtual Machine Honeypot Setup</h1>
Here we will set up 2 Azure Virtual Machines, 1 Windows and 1 Linux, to use in our Security Project as honeypots. We will disable the firewall protections at the Azure level locally in the Windows VM to open the machines to the internet.

<h2>Environments and Technologies Used</h2>

- Microsoft Azure
- Azure Network Security Groups (NSG)
- Windows Firewall Defender


<h2></h2>
 

<h2>Virtulal Machine Setup in Azure </h2>

<br />


<p>
1.  In Azure Create 2 VMs under the same Resource Group and on the same VNet. Make 1 Windows & 1 Linux.
</p>
<p>
<img src="https://i.imgur.com/QSn0enR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

  
[Click here to view instructions on how to create an Azure VM and access it using Remote Desktop](https://github.com/BryanEAtherton/Azure-Virtual-Machine)
</p>
<br />

<p>
2. Navigate to the Linux VM NSG and disable the Firewall by deleting the SSH inbound rule. 
</p>
<p>
<img src="https://i.imgur.com/CCWUnuQ.png" height="50%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/E7EQyPj.png" height="50%" width="40%" alt="Disk Sanitization Steps"/>
</p>

<p>
 3. Create a new rule to allow all traffic into the VM.
</p>
<p>
<img src="https://i.imgur.com/3NPTV98.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/8iTnSg6.png" height="50%" width="40%" alt="Disk Sanitization Steps"/>
</p>

<p>   
4. Repeat the process in step 2 for the Windows VM by deleting the RDP inbound rule.
<p>
<img src="https://i.imgur.com/vYFfEl4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
5. Repeat step 3 for the Windows VM and create a new rule to allow all traffic into the VM.
<p>
<img src="https://i.imgur.com/EoHjiaZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h2> Disable Windows Firewall Protections </h2>

<br />

<p>
1.  Here we can see a failed Ping attempt on the Windows VM because the local Firewall protections are active. 
</p>
<img src="https://i.imgur.com/3aQPBRc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<p>
2. RDP into the Windows VM, open Windows Defender Firewall, and select Windows Defender Firewall Properties. 
</p>
<p>
<img src="https://i.imgur.com/UZYoWJY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

[Click here to view instructions on how to create an Azure VM and access it using Remote Desktop](https://github.com/BryanEAtherton/Azure-Virtual-Machine)

<br />


<p>
 3. On the Domain, Public, and Private tabs, turn the firewall state to "off." Then select Apply, then Ok.
</p>
<p>
<img src="https://i.imgur.com/ArXHVD8.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/yHe1C81.png" height="50%" width="40%" alt="Disk Sanitization Steps"/>
</p>

<p>   
4. Windows will show an alert message that the Firewall is off, and Ping attempts on the Windows VM will now be successful.
</p>
<p>
<img src="https://i.imgur.com/MLI0f2I.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/zfCSDTh.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>


[Click here to return to the Security Project 1 Homepage](https://github.com/BryanEAtherton/Security-Project-1)
</p>
<br />





