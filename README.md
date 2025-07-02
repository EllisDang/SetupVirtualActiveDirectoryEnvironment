# Setup Virtual Active Directory Environment

<h2>Languages</h2>

- <b>PowerShell</b> 

<h2>Initial Setup: Downloading Oracle VM VirtualBox, Oracle VM VirtualBox Extension Pack, Server 2019 ISO, and Windows 10 ISO 64-bit</h2>

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
<img src="https://i.imgur.com/tbacJh6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/PgIf9Gv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">
Click Internet Icon (Bottom Right) > Change adapter options > Rename Ethernet 1 (Internet) and Ethernet 2 (Internal) > click on Internal (Properties) > IPv4 > Use the following IP address IP address (172.16.0.1) > Subnet mask (255.255.255.0) > Preferred DNS Server (127.0.0.1) > Right click start button (System) > Rename PC (DC) > Restart PC
<br />
<br />

<p align="center">
Adding Active Directory: <br/>

<p align="center">  
<img src="https://i.imgur.com/aiZyklk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/KxcByCk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">
Server Manager > Add roles and features > Next > Active Directory Domain Services > Next > Install > Click Caution Flag (Top right) > Promote this server to a domain controller > Add new forest > Root domain name (mydomain.com) > Add password > Next > Install > Restart
<br />
<br />

<p align="center">
Create dedicated domain admin account: <br/>

<p align="center">  
<img src="https://i.imgur.com/Db0AYFl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/AO5CgmW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/ZmF8rld.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/pbPeR0g.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/w6Onv8h.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/RCOx68A.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/RlbOkLx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/NW62b1v.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">
Start button > Windows Administrative Tools > Active Directory Users and Computers > Right click mydomain.com > New > Organizational Unit (_ADMINS) > Right click (_ADMINS) > New > User > Add your name > User login name (EX: a-edang) > Next > Password > Uncheck (User must change password at next logon) > Check (Password never expires) > Right Click User you just created > properties > Member Of > Add > Type (domain admins) > Check Names > Apply > Ok > Sign Out > Other User > (EX: a-edang)
<br />
<br />


<p align="center">
Installing RAS/NAT: <br/>

<p align="center">  
<img src="https://i.imgur.com/KQmzmxU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/KQmzmxU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">
Add roles and features > Next > Remote Access > Routing > Next > Install > Tools > Routing and Remote access > Right clic DC (local) > Confidure and Enable Routing and Remote Access > Network Address Translation (NAT) > Redo steps if Public interface doesn't pop up > Select "INTERNET" > Finish

<p align="center">
DHCP server <br/>

<p align="center">  
<img src="https://i.imgur.com/yYXAAXt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/0Vk6RIE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/4qGmyhK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/onTFJa4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/7mQfagH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">
Add roles and features > Next > DHCP Server > Next > Tools > DHCP > Expand (dc.mydomain) > Righ click IPv4 > New Scope > Name (172.16.0.100-200) > Next > Start IP address (172.16.0.100) > End IP address (172.16.0.200) > Length (24) > Subnet Mask (255.255.255.0) Next > Router (default Gateway) (172.16.0.1) > Add > Next > Finish
<br />
<br />

<p align="center">
Create User using PowerShell: <br/>

<p align="center">  
<img src="https://i.imgur.com/kAuOCYP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/3BdvaxS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
<p align="center">  
<img src="https://i.imgur.com/gY9U3qh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/N4fKrht.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/fBxLdKK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/cEvW8f9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/eHUGCWh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/cqs7CgB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/J8b5ojv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">
Server Manager > Configure this local server > IE Enhanced Sercurity Configuration > Turn Everything Off > Open Explorer > Paste Link (https://github.com/joshmadakor1/AD_PS/archive/master.zip) > Save as > Desktop > Drag File out to desktop > Open AD-PS-master > Names > add you name > Start button > Windows PowerShell > Right click Windows Power Shell ISE > More > run as admin > Paste power shell script from the folder > Set-ExecutionPolicy Unrestricted > Yes to all > cd C:\users\a-edang\desktop\AD-PS-master > Run script
<br />
<br />

<p align="center">
Create Windows 10 VM: <br/>

<p align="center">  
<img src="https://i.imgur.com/18LnvFi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/VHtue0N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/G1UC7yj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/W0ea3ng.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">
Oracle VM VirtualBox Manager > Name (CLIENT1) > Version (Windows 10 (64-bit) > Settings > System > Memory (4096 MB) > Processor (4) Advanced > Change both to "Bidirectional" > Network (Internal Network) > Start VM > Add Windows 10 ISO Downloaded above > I don't have product key > Windows 10 Pro > Custom install > Next > I don't have internet > Name (user) > next > command line > check connection by typing "Ipconfig" 
<br />
<br />

<p align="center">
Rename Windows 10 VM Hostname: <br/>

<p align="center">  
<img src="https://i.imgur.com/DrAOYXQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">  
<img src="https://i.imgur.com/jma65hh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">
Right click start button > System > Rename this PC (Advanced > Computer name (CLIENT1) > Member of Domain (mydomain.com) > Ok > Username (edang) > Password
<br />
<br />

<p align="center">
Logging on to User account that you created: <br/>

<p align="center">  
<img src="https://i.imgur.com/W85K9WJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">
CLIENT1 > sign out > EX: edang > Password
<br />
<br />





