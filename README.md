<h1> Setting up Microsoft Remote Desktop </h1>

<h2>Lab Objective </h2>
Understand how to set and work with Microsoft’s Remote Desktop Protocol (RDP).
By Establishing a remote connection to a computer with a user who has admistritive privilage.  
<br />

<h2>Languages and Utilities Used</h2>

- <b>Remote Desktop Protocol</b> 


<h2>Environments Used </h2>

- <b>VirtualBox Virtual Machines Machines (VM)<br />
 - <b>Windows 10 <br />
 - <b>Windows 7 <br />

<h2>Lab Walk-through:</h2>
<p align="left">
<h3> Lab Task 1: Enviorment Configuration </h3>  

<p align="center">
Select the appropriate VMs one at a time and click on the Settings button as shown below. (You will need to do this for the Windows 7 and Windows 10 VMs, one at a time.) <br/>
<img src="https://imgur.com/WMpPpYH.png" height="80%" width="80%" alt="RDP"/>
<br />
<br />
On the Windows 7 and 10 machines, select Internal Network.
<img src="https://imgur.com/1b2ovwG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
On the Windows 7 machine, configure the following settings and restart the machine: <br />
 -Computer Name: Client 7 <br />
 -IP address: 10.0.0.3 <br />
 -Windows Firewall: Off <br />
 <br />
Open the Control Panel and navigate to System and Security > System.
Click Change settings, then “Change …” to change the computer name.
Note: After changing the computer name, you will be prompted to restart the
machine. Accept the restart.
<img src="https://imgur.com/wP7rOkk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/2RS7erf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Navigate to Network and Internet via the Control Panel. Click Change
adapter settings to access the Local Area Connection properties and set a
static IP address of 10.0.0.3 with a netmask of 255.255.255.0.
Note: Select “Use the following IP address.”  <br/>
<img src="https://imgur.com/HNWZUcF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/IrsM7LT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<br />
<br />
Navigate to Network and Internet > Network and Sharing Center via the
Control Panel to open the Windows Firewall settings. Click Turn Windows
Firewall on or off and set it to off  <br/>
<img src="https://imgur.com/9d4lnd5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/ZW2STUW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Like on the Windows 7 machine, configure the following settings and restart the PC:  <br/>
 -Computer Name: Client10 <br/>
 -IP address: 10.0.0.4 <br/>
 -Windows Firewall: Off <br/>
 <br />
 Open the Control Panel and navigate to System and Security > System.
Click Change settings, then “Change …” to change the computer name.
Note: After changing the computer name, you will be prompted to restart the
machine. Accept the restart
<img src="https://imgur.com/0UWcdmM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/rxfD0nB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Set the static IP for the Windows 10 VM to 10.0.0.4
with a subnet mask of 255.255.255.0.  <br/>
<img src="https://imgur.com/gkVHGI9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/pq3Oucp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Turn off the Windows Firewall
<img src="https://imgur.com/r5nj3eq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/hhm8MU8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
Run ping from the Windows 10 machine to the Windows 7 machine to verify
connectivity.
<img src="https://imgur.com/MRWvTqV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
<p align="left">
<h3> Lab Task 2: Enable Remote Connection </h3>  

<p align="center">
Open Control Panel, navigate to System and Security > System, and click Remote
settings. Choose Allow connections from computers running any version of
Remote Desktop to enable the remote desktop on Client7.
<img src="https://imgur.com/VfdFc9N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
Add a new user to Client7 and add the user to the Administrators group in CMD,
with administrative privileges. <br />
Examples: <br />
- net user test Pa$$w0rd /ADD <br />
- net localgroup administrators test /ADD <br />
<img src="https://imgur.com/laW8N9t.png" alt="Disk Sanitization Steps"/>
<br />
<br /> 
<p align="left">
<h3> Lab Task 3: Establish Remote Connection </h3>  

<p align="center">
On the Windows 10 machine, look up “rdp” using the search field, and open the
Remote Desktop Connection application.
<img src="https://imgur.com/mQ8O2ul.png" alt="Disk Sanitization Steps"/>
<br />
<br /> 
Enter the IP address of the Windows 7 VM to establish the connection.
<img src="https://imgur.com/M0FER0C.png" alt="Disk Sanitization Steps"/>
<br />
<br /> 
Enter the credentials of a user on the Client7 machine to create a connection.
<img src="https://imgur.com/CxLE6zH.png" alt="Disk Sanitization Steps"/>
<br />
<br /> 
When a warning message saying the certification is unauthorized appears, accept
the connection by clicking Yes.
<img src="https://imgur.com/eOU6TfU.png" alt="Disk Sanitization Steps"/>
<br />
<br /> 
In the logon message, click Yes...................................................................................................................................
<img src="https://imgur.com/LYqR0xY.png" alt="Disk Sanitization Steps"/>
<br />
<br /> 
On the Windows 7 client, click OK................................................................................................................................
<img src="https://imgur.com/r6zNEQo.png" alt="Disk Sanitization Steps"/>
<br />
<br /> 
Note that you are now remotely connected to the machine.
<img src="https://imgur.com/tq2XXC2.png" alt="Disk Sanitization Steps"/>
<br />
<br />
To practice working with a remote connection, create a file on the desktop.
<img src="https://imgur.com/ogTDUtZ.png" alt="Disk Sanitization Steps"/>
<br />
<br />
<p align="left">
<h3> Lab Task 3: Safe Disconnection </h3>  

<p align="center">
Open the Start menu by clicking the Windows logo at the bottom left corner of
the screen. <br />
Click Log off on the right and select Disconnect
<img src="https://imgur.com/vwTUpI3.png" alt="Disk Sanitization Steps"/>
<br />
<br />
Log in to the Windows 7 client with the user selected for the remote connection
and note the file you created on the desktop
<img src="https://imgur.com/P3qRnjK.png" alt="Disk Sanitization Steps"/>
<br />
<br />
 
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
