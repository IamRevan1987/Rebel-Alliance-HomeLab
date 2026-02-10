# Current VM Lab setup notes

## Host Computer:
- BEELINK SER9 with AMD Ryzen 9 6900HX Radeon Graphics, 32GB RAM
- Microsoft Windows 11 Version 25H2 (OS Build 26200.7623)

## Host Server/VM1: RAS-Workstation-Alpha
- Location: C:\\Users\Rebel Alliance Lab\.VirtualBox\RAS-Workstation-Alpha
- OS: Windows Server 2022 (64-bit)
- DISK: 75GB
- PROCESSORS: 4
- RAM: 8GB

## Guest/VM2: RASWorkstationB
- Location: E:\\01 Active VMs\RASWorkstationB
- OS: Windows 10
- DISK: 50GB
- CORES: 4
- RAM: 8GB


## Guest/VM3: RAS-Core-UbuntuLinux
- Disc Location: 
- OS: Ubuntu Linux 24.02
- DISK: E:\\01 Active VMs\
- CORES: 
- RAM: 


## Guest/VM4: RAS-Core-KaliLinu
### This install will need another attempt at a later point.
- Disc Location:
- OS:
- DISK: 
- CORES: 
- RAM: 

# Logimetrics:

### Next steps:

- Fresh install VM3. 
- Established Users and OUs.
- Established 2 emails, one for `IT Admin` and one for `CEO`
- Established Proton Mail account for IT Admin. ***@proton.me
- Attaching "faux" website to the main server workstation.
- **RAS Website**: *www.RASai.net*


## February 10, Tuesday, 2026 - Initial Setup

### Steps ###:
The following procedure was execute for setup
- Install and boot Windows 2022 Server
- Establish Static IP Settings for server routing
- Shut down, switch network adapters, set video settings and ###SNAPSHOT### 
- Install Active Directory Domain Services and Restart
- Snapshot Here.
- Establish new DNS Server: RAS-WORKSTATION  Domain: alliance.net
- Downloaded IT Admin's "Installers" (Verified safe)
- Install DHCP/DNS Services, set scope, verify settings
- Install IIS Management services and setup Judy-Punk AI Website
- Confirm Network Signal with VM2..

- Install and boot Windows 10 (VM2)
- Shut down, switch network adapters, set video settings and ###SNAPSHOT###
- Boot up and access settings to connect to the domain.
- Verify domain connection with faux website.
- Verify domain connection by sharing a folder/file.

### Established Static Server IP Addressing as:
- 10.0.1.5
- 255.255.0.0
- 10.0.1.1
- FQDN: 5.1.0.10
- DNS: 192.168.0.1
- Name: RAS-Workstation-Alpha
- Workgroup: WORKGROUP












