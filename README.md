🔐 Azure Cloud Security Lab – Securing a Windows Server VM
📌 Project Overview

This project demonstrates the deployment, access, and security review of a Windows Server virtual machine in Microsoft Azure. The focus of the lab was to understand default cloud exposure, remote access risks, and basic network security controls in a cloud environment.

All resources were deleted after completion to ensure cost control and cloud hygiene.

🎯 Objectives

Deploy a Windows Server VM in Azure

Connect to the VM using native RDP

Identify security risks in default configurations

Review and understand Azure network security controls

Practice safe teardown of cloud resources

🏗 Architecture

Services Used:

Azure Virtual Machine (Windows Server)

Resource Group

Virtual Network (VNet)

Network Security Group (NSG)

Public IP Address

📸 Screenshot: VM overview and architecture

![VM Overview](screenshots/01-vm-overview.png.png)

⚙️ Environment Configuration

Region: East US

VM Size: Standard_B1s

OS Image: Windows Server 2019 Datacenter (x64 Gen2)

Security Type: Standard

Availability: No infrastructure redundancy

🔑 Access Method

The VM was accessed using Native RDP.

Connection Steps:

Navigated to the VM resource in Azure Portal

Selected Connect → RDP

Downloaded the RDP file

Connected using administrator credentials

📸 Screenshot: RDP connection settings

![RDP Connection](screenshots/03-rdp-connection.png.png)

⚠️ Security Risks Identified

Public RDP (Port 3389) exposed to the internet

VM accessible via public IP

No Just-In-Time (JIT) access enabled

No centralized logging or alerting configured

These risks reflect common real-world misconfigurations in cloud environments.

🔒 Security Controls Reviewed

Network Security Group inbound rules

Administrator credential complexity

VM networking configuration

Default Azure access recommendations

📸 Screenshot: NSG inbound rules

![NSG Rules](screenshots/02-nsg-rules.png.png)

🧠 Key Learnings

Azure defaults prioritize accessibility, not security

Public RDP access significantly increases attack surface

NSGs are the first line of defense for cloud VMs

Secure access methods (Bastion/VPN) are preferred in production

Proper teardown prevents unnecessary cloud costs

🔧 Recommended Improvements (Production Scenario)

Use Azure Bastion instead of public RDP

Enable Defender for Cloud

Configure Just-In-Time VM access

Restrict RDP to specific IP ranges

Enable Log Analytics and alerts

💰 Cost & Resource Management

Used burstable VM size for lab efficiency

VM and all associated resources deleted immediately after testing

Resource Group deletion used to ensure full cleanup

📂 Evidence

All screenshots were captured during the lab and stored in this repository.
Sensitive information has been redacted.

👤 Author

Name: Banele Ndlanzi
Focus Area: Cloud Security
Goal: Entry-level Cloud Security / SOC Analyst role
