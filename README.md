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

- Create Resource Group 
- Create 2 Virtual Machines
- Observe Traffic (ICMP, SSH, DHCP, DNS, RDP) 

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/tHGpmFH.png" height="80%" width="80%" alt="Virtual Machine Creation"/>
</p>
<p>
Using Azure, create a resource group followed with 2 virtual machines. The first VM operating on Windows and the second running on Linux.
</p>
<br />

<p>
<img src="https://i.imgur.com/4plaY3W.png" height="80%" width="80%" alt="ICMP"/>
</p>
<p>
Remote desktop connect into VM1 and then install Wireshark onto that. Filter for ICMP, and ping VM2. Observe the network traffic. 
</p>
<br />

<p>
<img src="https://i.imgur.com/SimoCCJ.png" height="80%" width="80%" alt="FireWall"/>
<p>
<img src="https://i.imgur.com/z03WRJ8.png" height="80%" width="80%" alt="FireWall"/>
<p>
Go into VM2's network security group and block ICMP traffic to observe the stop in traffic, as the firewall blocks access between the two networks. 
</p>
<br />

<p>
<img src="https://i.imgur.com/OXygwSy.png" height="80%" width="80%" alt="SSH"/>
</p>
<img src="https://i.imgur.com/THVGZrJ.png" height="80%" width="80%" alt="TCP.Port==22"/>
<p>
  </p>
<img src="https://i.imgur.com/BqlDG1p.png" height="80%" width="80%" alt="DNS/Udp.port==53"/>
<p>
Next, explore gaining access to the other computer's command line. Filter for SSH Traffic (tcp.port ==22), DNS (udp.port ==53), and RDP (tcp.port ==3389). 
</p>
<br />
