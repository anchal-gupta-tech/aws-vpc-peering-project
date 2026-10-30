# AWS VPC Peering Project

## Project Overview
This project demonstrates how to establish private communication between two Amazon Virtual Private Clouds (VPCs) using **VPC Peering** in AWS.

The setup includes a bastion host in VPC A and private EC2 instances in both VPCs. Connectivity is tested using SSH and ICMP (ping).

## AWS Services Used
- Amazon VPC
- Amazon EC2
- VPC Peering
- Internet Gateway
- Route Tables
- Security Groups

## Network Architecture

| Component | CIDR / Private IP |
|---|---|
| VPC A | `10.10.0.0/16` |
| Bastion Host | `10.10.1.10` |
| App-A | `10.10.2.10` |
| VPC B | `10.20.0.0/16` |
| App-B | `10.20.1.10` |

**AWS Region:** Asia Pacific (Sydney) — `ap-southeast-2`

## Implementation
1. Created two VPCs with separate CIDR blocks.
2. Configured public and private subnets.
3. Launched EC2 instances in the required subnets.
4. Created and activated a VPC Peering connection.
5. Configured route tables to enable communication between VPCs.
6. Configured security groups to control SSH and ICMP traffic.
7. Connected to the private App-B instance through the bastion host using SSH ProxyCommand.
8. Tested connectivity between App-A and App-B using ping.

## Connectivity Testing
- Tested ICMP connectivity between the private instances.
- Observed failed connectivity before the required security rule was enabled.
- Verified successful ping responses after the rule adjustment.
- Confirmed SSH access to App-B through the bastion host.

## Project Report
The complete project report, including AWS console and terminal screenshots, is available here:

[View / Download Project Report](./Anchal_Gupta_EWB_VPC_Peering.pdf)

## Key Learnings
- Understanding VPC architecture and subnetting.
- Configuring VPC Peering connections.
- Managing route tables and security groups.
- Accessing private EC2 instances through a bastion host.
- Troubleshooting network connectivity in AWS.

---

**Project by:** Anchal Gupta  
**College:** Graphic Era Hill University Dehradun
