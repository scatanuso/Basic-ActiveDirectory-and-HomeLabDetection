<h1>Active Directory Home Lab Detection</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
This project consists of demonstrating the creation of a simple Active Directory Domain Environment using Oracle Virtual Box. In addition, this project also showcases the use of Splunk, Sysmon, and Atomic Red Team (ATR) to generate telemetry on an Ubuntu Server running Splunk. This lab will simulate a real world attack by using an attack machine on the network running Kali Linux that will bruteforce a password from a user account on the Active Directory Domain environment. The goal of this project is to demonstrate thorough comprehension of how to configure Windows Machine, Splunk, and Active Directory while also emphaszing its role in a corporate network. In addition, demonstrating how a potential threat actor may compromise a coporate host system on the network, gaining access through the use of a password attack and stealing credentials.
<br />


<h2>Tools, Utilities, and Languages Used</h2>

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
<img src="https://i.imgur.com/WuVU9vN.png" height="80%" width="80%" alt="Logical Topology"/>
<br />
<br />
Installed and configured Splunk on Ubuntu Server and verified Splunk Service is actively running: <br/>
<img src="https://i.imgur.com/Ayh00zk.png" height="80%" width="80%" alt="Splunk Service"/>
<br />
<br />
Verified access to Splunk Web Interface er from Windows 10 Machine (Target-PC) and confirmed Splunk Server is working: <br/>
<img src="https://i.imgur.com/1HluQbQ.png" height="80%" width="80%" alt="Splunk Web Interface"/>
<br />
<br />
Logged into Splunk and configured a new index to receive the logs and events from Windows 10 Machine and Domain Controller: <br/>
<img src="https://i.imgur.com/v6MKyDF.png" height="80%" width="80%" alt="Configuered index"/>
<br />
<br />
Installed and configured Active Directory Domain Services on Windows 2022 Server and promoted server to domain Controller: <br/>
<img src="https://i.imgur.com/wfBwrzN.png" height="80%" width="80%" alt="Active Directory Server"/>
<br />
<br />
Creating Organizational Units and new user accounts:  <br/>
<img src="https://i.imgur.com/V9uJu89.png" height="80%" width="80%" alt="Organizational Units and User Accounts"/>
<br />
<br />
Logging into new user account on Windows 10 machine and verifying that it has joined the domain successfully: <br/>
<img src="https://i.imgur.com/kutvOjK.png" height="80%" width="80%" alt="Logging into new user account"/>
<br />
<br />
Using Kali Linux Attack Machine to perform brute force attack through the use of Crowbar on Host victim machine: <br/>
<img src="https://i.imgur.com/M6gn4C7.png" height="80%" width="80%" alt="Kali Linux Attack Machine"/>
<br />
<br />
View the generated telemetry or Events through Splunk:  <br/>
<img src="https://i.imgur.com/yEfon2w.png" height="80%" width="80%" alt="Splunk"/>
<br />
<br />
Identifying the source of the bruteforce attack on Splunk:  <br/>
<img src="https://i.imgur.com/nx6sLG9.png" height="80%" width="80%" alt="Splunk data and logs"/>
<br />
<br />
Using Atomic Red Team to generate data/logs by creating a new local user account and testing the security of Windows 10 target machine:  <br/>
<img src="https://i.imgur.com/kZxjlZY.png" height="80%" width="80%" alt="Atomic Red Team test"/>
<br />
<br />
Observe the NewLocalUser account on Splunk:  <br/>
<img src="https://i.imgur.com/pMs68St.png" height="80%" width="80%" alt="New Local User"/>
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
