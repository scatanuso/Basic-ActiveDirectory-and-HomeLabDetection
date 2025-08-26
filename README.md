<h1>Active Directory Home Lab Detection + Brute-force attack simulation</h1>

 ### [YouTube Demonstration](URL LINK TO VIDEO)

<h2>Description</h2>
This project consists of demonstrating the creation of a simple Active Directory Domain Environment using Oracle Virtual Box. In addition, this project also showcases the use of Splunk, Sysmon, and Atomic Red Team (ATR) to generate telemetry on an Ubuntu Server running Splunk. This lab will simulate a real world attack by using an attack machine on the network running Kali Linux that will bruteforce a password from a user account on the Active Directory Domain environment. The goal of this project is to simulate a corporate IT environment and gain hands on experience with Windows server administration. This project also demonstrates threat detection capabilities through the practual use of Splunk collecting logs and events from the Active Directory server and Windows 10 host machine. In addition, demonstrating how a potential threat actor may compromise a coporate host system on the network, gaining access through the use of a password attack and stealing credentials.
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
Created and configured virtual machines on VirtualBox: <br/>
<img src="https://i.imgur.com/NctPrT9.png" height="80%" width="80%" alt="Virtual Machines"/>
<br />
<br />
Installed Ubuntu server and modified the netplan configuration by statically assigning the IP address and other network parameters: <br/>
<img src="https://i.imgur.com/g9jWBTA.png" height="80%" width="80%" alt="netplan configuration"/>
<br />
<br />
Configured Splunk on Ubuntu Server and verified Splunk Service is actively running: <br/>
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
Installed Splunk Universal Forwarder and Sysmon and verified both services are running on both Windows 10 machine and Windows 2022 Server: <br/>
<img src="https://i.imgur.com/a3qPoMf.png" height="80%" width="80%" alt="Installed Splunk Universal Forwarder and Sysmon"/>
<br />
<br />
Verified that the new configured Index is revceiving logs and events from both Windows 10 Target Machine and Windows 2022 Server (ADDC01): <br/>
<img src="https://i.imgur.com/cOR7tGT.png" height="80%" width="80%" alt="Windows 10 and Server forwarding logs and events"/>
<img src="https://i.imgur.com/0nE1fOU.png" height="80%" width="80%" alt="Receiving events and logs"/>
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
Verifying Hydra is installed onto Kali Linux Machine. Hydra is the password cracking tool that will be used to perform a brute-force attack against the target machine: <br/>
<img src="https://i.imgur.com/wVCWQP4.png" height="80%" width="80%" alt="Installing Hydra"/>
<br />
<br />
Performing reconnaissance on Target-PC using nmap from the attacker machine (Kali Linux): <br/>
<img src="https://i.imgur.com/0HFYGek.png" height="80%" width="80%" alt="Using Nmap to perform network reconnassance"/>
<br />
<br />
Using Kali Linux Attack Machine to perform brute-force attack using Hydra to exploit RDP service on Windows 10 host machine and steal credentials: <br/>
<img src="https://i.imgur.com/c8MWWKK.png" height="80%" width="80%" alt="Launching attack"/>
<br />
<br />
Analyzing the events received on Splunk. Performing networking monitoring and analysis:  <br/>
<img src="https://i.imgur.com/2SBxY5L.png" height="80%" width="80%" alt="Splunk"/>
<br />
<br />
Identifying the source of the bruteforce attack on Splunk:  <br/>
<img src="https://i.imgur.com/Fuz6RZK.png" height="80%" width="80%" alt="Splunk data and logs"/>
<br />
<br />
Performing deep researching and viewing additional information on Splunk about the brute-force attack: <br/>
<img src="https://i.imgur.com/8kAjOxa.png" height="80%" width="80%" alt="Splunk data and logs"/>
<br />
<br />
Installing Atomic Red Team via Powershell to execute scripts for security testing: <br/>
<img src="https://i.imgur.com/Isv0nee.png" height="80%" width="80%" alt="Installing Atomic Red Team"/>
<br />
<br />
Setting an exclusion on the entire C-Drive of the Windows 10 host machine to prevent Microsoft Defender from detecting and removing the installed atomic red team files: <br/>
<img src="https://i.imgur.com/ja4Tf4Y.png" height="80%" width="80%" alt="Setting exclusion on C-Drive"/>
<br />
<br />
Using Atomic Red Team to generate data/logs by creating a new local user account and testing the security of Windows 10 target machine. T1110.001 is a script brute-force attack:  <br/>
<img src="https://i.imgur.com/JCgKADe.png" height="80%" width="80%" alt="Executing scripts"/>
<br />
<br />
Executing script to create a New Local Account on the network. T1136.001 is a script that creates a new LocalUserAccount:  <br/>
<img src="https://i.imgur.com/QA6igfi.png" height="80%" width="80%" alt="Creating a new local user account"/>
<img src="https://i.imgur.com/InyuARc.png" height="80%" width="80%" alt="Creating a new local user account"/>
<br />
<br />
Analyzing the events recorded from Splunk to identify the new local account: <br/>
<img src="https://i.imgur.com/qUneS2I.png" height="80%" width="80%" alt="New Local User"/>
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
