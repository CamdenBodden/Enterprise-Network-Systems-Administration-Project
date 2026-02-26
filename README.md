<p align="center"> 
  <img src="images/Project_Header.jpg" width="1000" height="300"/>
</p> 
<h1>Enterprise Network & Systems Administration Project</h1>
<h2>Environments and Technologies Used</h2>

- Fortinet FortiGate Firewall
- Fortinet FortiSwitch
- Fortinet FortiAP (Wireless)
- Microsoft Hyper-V
- Windows Server
- Active Directory Domain Services
- DNS
- DHCP
- Group Policy
- File Services
- VLAN Segmentation

<h2>Operating Systems Used</h2>

- Windows Server
- Windows Client OS

<h2>Project Overview</h2>

This project is a fully designed enterprise-style infrastructure environment built to simulate real-world network and systems administration.

The environment demonstrates centralized identity management, secure network segmentation, role-based access control, and structured file services using industry standard enterprise technologies.

This lab includes:

- Active Directory domain infrastructure
- Redundant domain controllers
- DNS and DHCP services
- Department-based file storage
- Group Policy deployment
- VLAN network segmentation
- Firewall-controlled inter-VLAN routing
- Administrative delegation model
- Least-privilege security design

The objective is to build, secure, and manage a scalable enterprise environment from the network layer through identity and access control.

<h2>Part 1 — Physical & Network Architecture</h2>

The infrastructure is built around a layered network model:
- FortiGate performs routing and security policy enforcement
- FortiSwitch provides access layer connectivity
- FortiAP delivers segmented wireless networks
- Hyper-V hosts the virtual server infrastructure
Network segmentation is implemented using VLANs:

| VLAN | Purpose            |
|------|-------------------|
| 10   | Management        |
| 20   | Servers           |
| 30   | Workstations      |
| 40   | Corporate Wireless|
| 50   | Guest Wireless    |

Traffic between networks is controlled through firewall policy using least-privilege principles.

<p align="center"> 
<img src="images/Network_Toplogy.jpg" width="1000" height="500"/>
</p>

<h2>Part 2 — Virtual Server Infrastructure (Hyper-V)</h2>

Virtual machines were deployed to provide enterprise services:
- Domain Controller 1 (Primary)
- Domain Controller 2 (Redundancy)
- File Server
- Domain-joined Client workstation

Each system was assigned appropriate network segmentation and configured for domain integration.

<p>
<img src="images/Hyper-V_Virtual_Machines.png" width="1000" height="350"/>
</p>

<h2>Part 3 — Active Directory Domain Services Deployment</h2>

The domain environment was created to centralize authentication, authorization, and policy management.

Configuration included:
- Forest and domain creation
- Organizational Unit structure
- Administrative delegation
- Security group hierarchy
- Domain controller redundancy

<p>
<img src="images/Active_Directory_OU_Structure.png" width="1000" height="500"/>
</p>

<h2>Part 4 — Identity & Access Management Model</h2>

Access control follows a structured group nesting strategy to support scalable permission management.
Implementation includes:
- Role-based security groups
- Departmental access separation
- Administrative privilege delegation
- Least-privilege enforcement

<p>
  <img src="images/Security Groups.png" width="1000" height="500"/>
</p>

<h2>Part 5 — File Services & Department Storage</h2>

Centralized file storage was implemented using structured share design.

Configuration includes:
- Department file shares
- User home directories
- NTFS permission enforcement
- Share permission alignment
- Group-based access control

<p>
  <img src="images/File_Share_Structure.png" width="1000" height="700"/>
</p>

<h2>Part 6 — Group Policy Deployment</h2>

Group Policy was used to standardize configuration and automate resource access.

Policies include:
- Drive mapping for department shares
- Home directory mapping
- User configuration management
- Administrative control settings

<p> PLACE SCREENSHOT HERE — Group Policy Management Console </p>


