<h1>Active Directory Project</h1>

<h2>Description</h2>
In this project the purpose is to create an Active Directory (AD), Domain Controller, DHCP server, and to add a client to the domain.

<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b>
- <b>Oracle VirtualBox</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)
- <b>Windows Server 2019</b>

<h2>Concepts </h2>

- <b>Active Directory</b> 
- <b>Domain Controller</b>
- <b>DHCP Server</b>
- <b>IP Address</b>

<h2>Program walk-through:</h2>

<p align="left">
Step 1: Using Oracle VirtualBox to set up the Windows Server and Client Virtual Machines. <br/>
<img src="https://i.imgur.com/hWTwwfr.png" height="80%" width="80%" alt="Virtual Machines"/>
<br />
<br />
Step 2: Logging into the Windows Server VM, I am configuring the Network Adapters. As on display the Intranet Network is set to have the following IP address and to use the "Preferred DNS server" address.
 
Important: Having a two Network adapters setup, the first one to provide the Domain's internet by the ISP. And the second one, an Intranet Network, for all the Domain userU. <br/>
<img src="https://i.imgur.com/wEq20IL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 3: Adding Active Directory Domain Services.

Important: It is significant that we are able to assign roles for our users. This provides them with the centralized authentication and authorization to the network and network resources. <br/>
<img src="https://i.imgur.com/f3hU4Xq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 4: Creating an Organizational Unit (OU) for my Admins within the Domain Controller. In the OU, ADMINS, I’ve also created a User, Solid Snake, who will have admin privileges to manage my Active Directory. To achieve this the User will be assigned into “Member of” the “Domain.Admins.” 

Important: Do NOT work within the Active Directory server, itself, to prevent any security/server issues.   <br/>
<img src="https://i.imgur.com/27fPypc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 5: After swapping into the Admin User it is time to set up the Dynamic Host Configuration Protocol (DHCP) for the Domain. The IPv4 is configured to have the "Scope" of IP address ranging from 100-200 and then "refreshed: to apply the changes. Follow those steps the Domain will also need to be “authorized” to finalize the setup.

Important: The significant of having a DHCP server is to automatically assign IP addresses for my Users/ Clients that are assigned on the domain.<br/>
<img src="https://i.imgur.com/AEwdYLD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 6: Creating a Router so that the Users/ Clients are able to connect and communicate to the DNS server of the domain.   <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
