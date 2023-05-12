<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

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
- Step 4

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/tHGpmFH.png" height="80%" width="80%" alt="Virtual Machine Creation"/>
</p>
<p>
Using Azure, I created 2 virtual machines. The first operating on Windows and the second running on Linux.
</p>
<br />

<p>
<img src="https://i.imgur.com/4plaY3W.png" height="80%" width="80%" alt="ICMP"/>
</p>
<p>
I then installed Wireshark and first filterd for ICMP. With the assistance of Powershell, I observed png request and replies within Wireshark. I then did a non stop ping (-t).
</p>
<br />

<p>
<img src="https://i.imgur.com/SimoCCJ.png" height="80%" width="80%" alt="FireWall"/>
<p>
<img src="https://i.imgur.com/z03WRJ8.png" height="80%" width="80%" alt="FireWall"/>
<p>
I then did a nonstop ping and created a firewall in National Secrutiy Groups, to block incoming traffic from that server. 
</p>
<br />

<p>
<img src="https://i.imgur.com/OXygwSy.png" height="80%" width="80%" alt="SSH"/>
</p>
<img src="https://i.imgur.com/THVGZrJ.png" height="80%" width="80%" alt="TCP.Port==22"/>
<p>
  </p>
<img src="https://i.imgur.com/BqlDG1.png" height="80%" width="80%" alt="DNS/Udp.port==53"/>
<p>
Next, I explored gaining access to the other computers command line. I filtered for SSH Traffic (tcp.port ==22) and DNS (udp.port ==53). 
</p>
<br />
