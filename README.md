<h1>SIEM | Honeypot RDP Home Lab</h1>

<h2>Description</h2>
Project consisted of setting up Microsoft Sentinel in Azure (SIEM). I connected the SIEM to a live virtual machine configured as a honeypot. I observed live attacks from all over the world that were logged as audit failures (RDP brute force attacks) on the VM. I utilized a custom PowerShell script to identify attackers' geolocation information and plotted it on the Microsoft Sentinel map.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>SIEM</b>
- <b>Microsoft Sentinel</b>
- <b>Honeypot</b>
- <b>Remote Desktop Protocol</b>

<h2>Environments Used </h2>

- <b>Windows 11</b>
- <b>Virtual Machine </b>

<h2>Project Walk-through:</h2>

<p align="center">
Create Virtual Machine in Azure: <br/>
<img src="https://i.imgur.com/1gvX7JN.png"/>
<br />
<br />
Create Log Analytics Workspace:  <br/>
<img src="https://i.imgur.com/a2BDXnq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Connect VM to Log Analytics: <br/>
<img src="https://i.imgur.com/3EAn1QB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe Event Viewer Logs in VM:  <br/>
<img src="https://i.imgur.com/j9k0Bgp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Turn off Firewall on VM to expose VM to internet (honeypot):  <br/>
<img src="https://i.imgur.com/bDCkKHZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Ping VM IP from Command Prompt:  <br/>
<img src="https://i.imgur.com/kjHKiuT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Link Geolocation.io API Key:  <br/>
<img src="https://i.imgur.com/FBe0ElC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Modify Log Analytics Custom Fields to Train the Algorithm to Pull Correct Latitude and Longitude Data Points:  <br/>
<img src="https://i.imgur.com/SweqABX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Extract Fields from Raw Custom Data Log:  <br/>
<img src="https://i.imgur.com/OCZ0Nrj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Set up Map Query in Sentinel with Latitude and Longitude :  <br/>
<img src="https://i.imgur.com/9RGBrPZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure Map Settings in Sentinel to Pin Failed Login Attempts on Map:  <br/>
<img src="https://i.imgur.com/oY7gPgP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Final Failed Login count data (VM was live for only a few hours):  <br/>
<img src="https://i.imgur.com/xBVuAyo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
