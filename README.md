<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1
- Step 2
- Step 3

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/2QEVeWT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This is kinda connected to the other activity I did so check out the previous activity of these don't make sense. Login DC-1 as domain admin. Start->windows administrative tools->active directory users and compuers-> my domain.com->employees then pick a name to use make sure you use the display name to login. Login to the chosen account in client-1 and use the password you set. On DC-1 C:\drive create folders "read-access", "write-access", "no-access" and "accounting".
</p>
<br />

<p>
<img src="https://i.imgur.com/ezjCBN9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Give domain users access to read-access and write-access. Right click on folder->properties->sharing->share->type domain users->then select the permission read-access only read and write-access read/write. Give domain admins access to no-access right click no access->properties->sharing->share...->type domain admins->permission select read/write. Login client-1 find the folder with \\DC-1.
</p>
<br />

<p>
<img src="https://i.imgur.com/LffMfXt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we are going to see if the permissions work. Try writing in read-access and opening no-access no of those should work for you if followed the steps. Make "Accountant" role in organization unit and give access to read/write in accountant's folder. Now try accessing accountants from client-1. You can play around with this practice and do many things like try from the other end where it's supposed to work.
</p>
<br />
