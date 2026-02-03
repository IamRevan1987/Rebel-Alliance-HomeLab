*Current system notes:*

**Host Computer:**
BEELINK SER9 with AMD Ryzen 9 6900HX Radeon Graphics, 32GB RAM
Microsoft Windows 11 Version 25H2 (OS Build 26200.7623)

**Host Server/VM1: RAS-Workstation-Alpha**
Oracle VirtualBox 
Location: C:
OS: Windows Server 2022 (64-bit)
DISK: 75GB
PROCESSORS: 4
RAM: 8GB

**Guest/VM2: RASWorkstationB**
VMWare Pro
Disc Location: E:\01 Active VMs\01 
OS: Kali Linux
DISK: 100GB
CORES: 6
RAM: 8GB


**Guest/VM3: RAS-Core-UbuntuLinux**
VMWare Pro
Disc Location: E:\01 Active VMs\01 
OS: Kali Linux
DISK: 100GB
CORES: 6
RAM: 8GB


**Guest/VM3: RAS-Core-KaliLinu**
*** This install will need another attempt at a later point.
VMWare Pro
Disc Location: E:\01 Active VMs\01 
OS: Kali Linux
DISK: 100GB
CORES: 6
RAM: 8GB

**Logimetrics:
February 3, Tuesday, 2026 - Initial Setup

Starting with VM1 and VM2 fresh installs, setting up VM1 as the server.
Configuration is still the same, Active Directory is being setup for 8 users.
Successfully added VM2 to ALLIANCE.NET Domain
Created a real email account for the IT Admin, self, @ dave.it.stacey@proton.me
Created a real email account for Sales rep Leia Organa @ daveisrevan@zohomail.com
I have successfully added OUs and populated them accordingly.
Added web services to Active Directory.
Successfully added the fake website to the inetpub folder, loads successfully on localhost.
Established the website as www.alliance.com via IIS Manager.
Successfully installed VMs 3 Ubuntu Linux, and connected to the Domain, and verified the server website.

*Next steps:
Research Wazuh
Assign Users to Computers and define rules.


February 1, Sunday, 2026 - Initial Setup

Clearing out space on "DROID" removable HDD


Stopped VM building with fresh installs of VM1 and VM2, VM3 still needs to be installed. 
Focusing on setup of main office workstation and building of fake company website using AntiGravity Pro
Established Brave Browser for security and privacy.
Established Proton Mail account for IT Admin. ***@proton.me
** Must remember to setup other emails with Zoho Mail, recommended by ChatGPT

Established a Static Server IP Addressing as:
10.0.1.5
255.255.0.0
10.0.1.1
FQDN: 5.1.0.10
DNS: 192.168.0.1
Name: RAS-Workstation-Alpha
Workgroup: WORKGROUP



