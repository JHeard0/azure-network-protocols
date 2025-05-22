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
<img src="https://i.imgur.com/7SyzPuV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p></p>
Create a rule that denies ICMP traffic
<p></p>
<img src="https://i.imgur.com/L820qIl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p></p>

After the rule is created, it stops the flow of the perpetual pings, resulting in the request being timed out and no response being found in Wireshark.
<p></p>
<img src="https://i.imgur.com/YRckMBN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p></p>
<img src="https://i.imgur.com/3wEDlvc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p></p>
Get rid of the rule and observe the replies continue
<p></p>
<img src="https://i.imgur.com/iIUzOld.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p></p>

<h3> Observing SSH Traffic </h3>
<p></p>
From the Windows-VM SSH into the Linux-VM, then start typing
<p></p>
<img src="https://i.imgur.com/EwTRUdt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Every single time something is typed while logged in through SSH will transport data
<img src="https://i.imgur.com/uxKEEiD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<h3> Observing DHCP Traffic</h3>
<p></p>

Run the command "ipconfig /renew" on the Windows-VM
<p></p>
<img src="https://i.imgur.com/uxKEEiD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p></p>
What occurs here is the request to renew the IP, and the Domain Name System acknowledges the request
<p></p>
<h3> Observing DNS Traffic</h3>
<p></p>
Filtering for DNS traffic, nslookup Google & Disney
<img src="https://i.imgur.com/KY5ScbL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/TgAx7RX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p></p>
There is a log for each time the Windows VM checks a DNS server for the name until it is eventually found.
<p></p>


