# Setup Virtual Active Directory Environment

<h2>Languages</h2>

- <b>PowerShell</b> 

<h2>Initial Setup: Downloading VirtualBox, Oracle VM VirtualBox Extension Pack, Server 2019 ISO, and Windows 10 ISO 64-bit</h2>

VirtualBox: https://www.virtualbox.org/wiki/Downloads

Server 2019 ISO: https://www.microsoft.com/en-us/evalcenter/download-windows-server-2019

Windows 10 ISO 64-bit: https://www.microsoft.com/en-us/software-download/windows10

<h2>Project walk-through:</h2>

<p align="center">
Creating Domain Controller VM: <br/>
<img src="https://i.imgur.com/aalva1C.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/FSVgC9n.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/vndW60M.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">
New > Name (DC) > Version (Other Windows 64-bit) > Base Memory (2048 MB) > Processors (4) > Next > Finish
<br />
<br />

<p align="center">
Changing Settings: <br/>

<p align="center">  
<img src="https://i.imgur.com/gTSzoth.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/i0ktv3N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/TMp0Znp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/YpKxiYU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/tW7HynA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/WG2XT08.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/5l6BVic.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">
Expert > Advanced > Change both to "Bidirectional" > Network (Adapter 1 NAT) (Adapter 2 Internal Network) > Start VM > Add Server 2019 ISO Downloaded above > Windows Server 2019 Standard Evaluation (Desktop expericience) > Custom Install > Next
<br />
<br />

<p align="center">
Install VM guest additions: <br/>

<p align="center">  
<img src="https://i.imgur.com/xUjIMTw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/YCYVcdW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/FnGNHdS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">
Devices (up top) > Insert Guest Addition CD Image > Open File Explorer > This PC > CD Drive (D:) VirtualBox Guest Additons > VBoxWindowsAdditions-amd64 > Next All then Install > Manually reboot later > Shut Down VM
<br />
<br />

<p align="center">
Setting up Domain Controller IP Address and Renaming PC: <br/>

<p align="center">  
<img src="https://i.imgur.com/HWb2p41.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/Ts8aMKe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/nIwKKHU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/yjUUNOX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/MzhDRWl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">
Click Internet Icon (Bottom Right) > Change adapter options > Rename Ethernet 1 (Internet) and Ethernet 2 (Internal) > click on Internal (Properties) > IPv4 > Use the following IP address IP address (172.16.0.1) > Subnet mask (255.255.255.0) > Preferred DNS Server (127.0.0.1)
<br />
<br />






