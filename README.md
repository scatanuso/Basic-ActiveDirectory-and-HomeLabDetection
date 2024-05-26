<h1>Active Directory Home Lab Detection</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
This project consists of demonstrating the creation of a simple Active Directory Domain Environment using Oracle Virtual Box. In addition, this project also showcases the use of Splunk, Sysmon, and Atomic Red Team (ATR) to generate telemetry on Ubuntu Server running Splunk. This lab will simulate a real world attack by using an attack machine on the network running Kali Linux that will bruteforce a password from a user account on the Active Directory Domain environment. The goal of this project is to demonstrate thorough comprehension of how to configure Windows Machine, Splunk, and Active Directory while also emphaszing its role in a corporate network. In addition, demonstrating how a potential threat actor may compromise a coporate host system on the network, gaining access through the use of a password attack.
<br />


<h2>Operating Systems, Software, Tools, Utilities, and Languages Used</h2>

- <b>PowerShell</b> 
- <b>Splunk</b>
- <b>Sysmon</b>
- <b>Atomic Red Team</b>

<h2>Environments Used </h2>

- <b>Windows 2022 server</b> (21H2)
- <b>Windows 10</b> (21H2)
- <b>Kali Linux</b> (21H2)
- <b>Ubuntu Server</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
HomeLab Topology: <br/>
<img src="https://imgur.com/a/KQG4wvH" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
