<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computers)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Creating and observing traffic between Virtual machines
- Configuring a Firewall to obstruct and observe traffic


<h2>Actions and Observations</h2>

<h3>ICMP Traffic</h3>
<p>
Between Windows-VM (10.0.0.13) & Linux-VM (10.0.0.14)
<img src="https://i.imgur.com/EcamY0x.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
ICMP traffic between Windows-VM (10.0.0.13) & Google (10.0.0.14)
<p>
</p>
<img src="https://i.imgur.com/KmzQh6J.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>

<h3> Stopping ICMP Traffic with a Firewall</h3>
<p>
</p>
Start by initiating a perpetual ping to the Linux-VM (10.0.0.14)
<p>
</p>
<img src="https://i.imgur.com/7SyzPuV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><img src="https://i.imgur.com/7SyzPuV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
</p>

